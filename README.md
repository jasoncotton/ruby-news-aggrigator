# ruby-news-aggrigator
A simple news aggrigrator in Ruby on Rails.  Goal is to create a simple api/web-service to aggrigtate news into a single source.
## Design
The majority of the work can be found in the lib path, a generic news connector class is the interface/foundation for connecting to news sources.  Two different methods are needed to create a new connector:
1. get_url: should return the url to get the top news articles
2. transform: gets passed the response from the url (from #1) and should return an ordered list of news articles using the NewsWrapper::Article object.
