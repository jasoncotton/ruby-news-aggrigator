# ruby-news-aggrigator
A simple news aggrigrator in Ruby on Rails.  Goal is to create a simple api/web-service to aggrigtate news into a single source.
## Requirements
The code was developed with the following code (versions), I haven't tested any of the code with any versions other than those listed and cannot guarantee it would work otherwise, but it should.
*Ruby 1.9.3 (p484)
*Rails 4.1.8
## Design
The majority of the work can be found in the lib path, a generic news connector class is the interface/foundation for connecting to news sources.  Two different methods are needed to create a new connector:
1. get_url: should return the url to get the top news articles
2. transform: gets passed the response from the url (from #1) and should return an ordered list of news articles using the NewsWrapper::Article object.
## How to use:
To use the webservice, deploy the code out to a server that has access to the ruby and rails (versions listed above in this document), deploy using your favorite web server or use the rails server, (rails s) from within the project.
Accessing the webserver by pointing to your web server -- localhost:3000 in the case of rails s -- and either just hit the root path (/) or /news, /news.json or /news.html, news.html results in the scaffold view of the news, all other endpoints will result in the .json response.
