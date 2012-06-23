.. Physics documentation master file, created by
   sphinx-quickstart on Fri Oct 30 19:23:04 2009.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

News feed
=========

.. raw:: html

	<!--iframe src="http://davidpugal.blogspot.com" 
		height=600 width="100%"
		frameborder=0></iframe-->

	<ul id="entries"><li class="loading">Loading...</li></ul>
	  
	<script type="text/javascript" src="http://www.google.com/jsapi"></script>
	<script type="text/javascript">
	  
	  // ================================================
	  // Your info here
	  // ================================================
	  var feedURL   = 'http://davidpugal.blogspot.com//feeds/posts/default';
	  var numEntries  = 10;
	  var blogURL   = 'http://davidpugal.blogspot.com';
	  var blogLink  = 'View full blog';
	  // ================================================
	  
	  google.load("feeds", "1");
	  
	  function formatDate(d, f) {
	    var d = new Date(d);
	    var months = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'];
	    var days = ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'];
	    return f.replace(/(yyyy|mmmm|mmm|mm|dddd|ddd|dd|hh|nn|ss|a\/p)/gi,
		  function(\$1) {
		      switch (\$1.toLowerCase()) {
		      case 'yyyy': return d.getFullYear();
		      case 'mmmm': return months[d.getMonth()];
		      case 'mmm':  return months[d.getMonth()].substr(0, 3);
		      case 'mm':   return (d.getMonth() + 1);
		      case 'dddd': return days[d.getDay()];
		      case 'ddd':  return days[d.getDay()].substr(0, 3);
		      case 'dd':   return d.getDate();
		      case 'hh':   return ((h = d.getHours() % 12) ? h : 12);
		      case 'nn':   return d.getMinutes();
		      case 'ss':   return d.getSeconds();
		      case 'a/p':  return d.getHours() < 12 ? 'a' : 'p';
		      }
		  }
	      );
	  }
	  
	  function initialize() {
	    var feed = new google.feeds.Feed(feedURL);
		feed.setNumEntries(numEntries);
		feed.load(function(result) {
	  
		  if(result.error) return;
	  
		  var list = document.getElementById('entries');
		      list.removeChild(list.firstChild);
	  
		  for(var i = 0; i < result.feed.entries.length; i++) {
		    var entry = result.feed.entries[i];
		    var link = document.createElement('a');
			link.setAttribute('href', entry.link);
			link.appendChild(document.createTextNode(entry.title));
		    var title = document.createElement('h2');
			title.appendChild(link);
		    var date = document.createElement('p');
			date.setAttribute('class', 'blog_date');
			date.appendChild(document.createTextNode(formatDate(entry.publishedDate, 'mmmm dd, yyyy')));
		    var content = document.createElement('div');
			content.innerHTML = entry.content;
		    var li = document.createElement('li');
			li.appendChild(title);
			li.appendChild(date);
			li.appendChild(content);
		    list.appendChild(li);
		  }
	  
		  if(blogLink && blogURL) {
		    var link = document.createElement('a');
		      link.setAttribute('href', blogURL);
		      link.innerHTML = blogLink;
		    var li = document.createElement('li');
		      li.appendChild(link);
		    list.appendChild(li);
		  }
	      });
	  }
	  
	  google.setOnLoadCallback(initialize);
	  
	</script>


.. toctree::
    :hidden:
    :maxdepth: 3

    self
    src/contact
    src/experience
    src/projects
    src/notes
..    src/research


