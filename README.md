# cloudgo
# curl test

    *Trying 127.0.0.1...
    *Connected to localhost (127.0.0.1) port 8080 (#0)
    > GET /hello/testuser HTTP/1.1
    > Host: localhost:8080
    > User-Agent: curl/7.47.0
    > Accept: */*
    >
    < HTTP/1.1 200 OK
    < Content-Type: application/json; charset=UTF-8
    < Date: Wed, 15 Nov 2017 06:39:19 GMT
    < Content-Length: 30
    <
    {
    "Tes": "Hello testuser"
    }
    * Connection #0 to host localhost left intact

# abtest 参数解释 

- -n:请求数
- -c:并发请求数

# ab test 1

    This is ApacheBench, Version 2.3 <$Revision: 1706008 $>
    Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
    Licensed to The Apache Software Foundation, http://www.apache.org/

    Benchmarking localhost (be patient)
    Completed 100 requests
    Completed 200 requests
    Completed 300 requests
    Completed 400 requests
    Completed 500 requests
    Completed 600 requests
    Completed 700 requests
    Completed 800 requests
    Completed 900 requests
    Completed 1000 requests
    Finished 1000 requests


    Server Software:        
    Server Hostname:        localhost
    Server Port:            8080

    Document Path:          /hello/your
    Document Length:        26 bytes

    Concurrency Level:      100
    Time taken for tests:   0.700 seconds
    Complete requests:      1000
    Failed requests:        0
    Total transferred:      149000 bytes
    HTML transferred:       26000 bytes
    Requests per second:    1427.84 [#/sec] (mean)
    Time per request:       70.036 [ms] (mean)
    Time per request:       0.700 [ms] (mean, across all concurrent requests)
    Transfer rate:          207.76 [Kbytes/sec] received

    Connection Times (ms)
                  min  mean[+/-sd] median   max
    Connect:        0    4  13.7      0      95
    Processing:     1   57  19.8     61     104
    Waiting:        1   57  19.8     61     104
    Total:          1   61  17.0     62     115

    Percentage of the requests served within a certain time (ms)
      50%     62
      66%     65
      75%     67
      80%     69
      90%     85
      95%     94
      98%    100
      99%    104
     100%    115 (longest request)

# ab test 2

    This is ApacheBench, Version 2.3 <$Revision: 1706008 $>
    Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
    Licensed to The Apache Software Foundation, http://www.apache.org/

    Benchmarking localhost (be patient)
    Completed 500 requests
    Completed 1000 requests
    Completed 1500 requests
    Completed 2000 requests
    Completed 2500 requests
    Completed 3000 requests
    Completed 3500 requests
    Completed 4000 requests
    Completed 4500 requests
    Completed 5000 requests
    Finished 5000 requests


    Server Software:        
    Server Hostname:        localhost
    Server Port:            8080

    Document Path:          /hello/your
    Document Length:        26 bytes

    Concurrency Level:      200
    Time taken for tests:   4.262 seconds
    Complete requests:      5000
    Failed requests:        0
    Total transferred:      745000 bytes
    HTML transferred:       130000 bytes
    Requests per second:    1173.22 [#/sec] (mean)
    Time per request:       170.471 [ms] (mean)
    Time per request:       0.852 [ms] (mean, across all concurrent requests)
    Transfer rate:          170.71 [Kbytes/sec] received

    Connection Times (ms)
                  min  mean[+/-sd] median   max
    Connect:        0   44 205.3      0    1036
    Processing:     0  124  48.2    125     357
    Waiting:        0  124  48.2    125     357
    Total:          0  167 219.8    127    1307

    Percentage of the requests served within a certain time (ms)
      50%    127
      66%    141
      75%    152
      80%    161
      90%    189
      95%    266
      98%   1222
      99%   1246
     100%   1307 (longest request)
