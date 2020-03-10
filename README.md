### Debug toolbar tabs problem
Special case showing debug toolbar exception with nginx server configured as reversed proxy


#### Init
* docker-compose up
* docker-compose exec symfony composer install

#### Case reconstruction

1) Browse any project url, so debug toolbar will load.

2) Use one of debug toolbar menu tabs, for example which show time of execution

3) You should get error similar to this from the screen. 