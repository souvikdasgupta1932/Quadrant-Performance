Command used for execution:
k6 run script.java

Input: 
For 15s we are increasing the users and reaching 100.
Then for the next 30s, constant 100 users is maintained.
Then for the next 15s, the users are decreased to 0.

Output:
 scenarios: (100.00%) 1 scenario, 100 max VUs, 1m30s max duration (incl. graceful stop):
           * default: Up to 100 looping VUs for 1m0s over 3 stages (gracefulRampDown: 30s, gracefulStop: 30s)


running (1m00.9s), 000/100 VUs, 4265 complete and 0 interrupted iterations
default ✓ [======================================] 000/100 VUs  1m0s

     ✓ status was 200

     checks.........................: 100.00% ✓ 4265      ✗ 0
     data_received..................: 36 MB   588 kB/s
     data_sent......................: 421 kB  6.9 kB/s
     http_req_blocked...............: avg=4.01ms   min=0s      med=0s       max=284.93ms p(90)=0s       p(95)=0s
     http_req_connecting............: avg=1.27ms   min=0s      med=0s       max=70.45ms  p(90)=0s       p(95)=0s
     http_req_duration..............: avg=61.2ms   min=50.04ms med=59.37ms  max=373.59ms p(90)=66.39ms  p(95)=70.25ms
       { expected_response:true }...: avg=61.2ms   min=50.04ms med=59.37ms  max=373.59ms p(90)=66.39ms  p(95)=70.25ms
     http_req_failed................: 0.00%   ✓ 0         ✗ 4265
     http_req_receiving.............: avg=792.34µs min=0s      med=509.49µs max=171.43ms p(90)=1.06ms   p(95)=1.52ms
     http_req_sending...............: avg=146.47µs min=0s      med=0s       max=3.89ms   p(90)=552.67µs p(95)=650.74µs
     http_req_tls_handshaking.......: avg=2.71ms   min=0s      med=0s       max=226.77ms p(90)=0s       p(95)=0s
     http_req_waiting...............: avg=60.26ms  min=48.88ms med=58.57ms  max=373.44ms p(90)=65.49ms  p(95)=69ms
     http_reqs......................: 4265    70.050641/s
     iteration_duration.............: avg=1.07s    min=1.05s   med=1.06s    max=1.37s    p(90)=1.07s    p(95)=1.08s
     iterations.....................: 4265    70.050641/s
     vus............................: 6       min=6       max=100
     vus_max........................: 100     min=100     max=100
	 
	 
Explanation:
4265 tests were conducted over the course of 60s
http_req_duration on an average is 61.2ms, the demand on the server has caused the server to slow down to fullfill the request.
