# prometheus_training

engine_daemon_container_states_containers

engine_daemon_container_states_containers{state="running"}

up{region="IN"}

sum ( up{region="IN"} )

# range vector example
node_memory_MemFree_bytes{env="prod"}[10m]

# instant vector example
node_memory_MemFree_bytes{env="prod"}

node_memory_MemFree_bytes{env!="prod"}

process_cpu_seconds_total{job=~"linuxnode.*"}

process_cpu_seconds_total{job!~"linuxnode.*"}

prometheus_http_requests_total{handler=~"/api.*"}

prometheus_http_requests_total{handler=~"/api.*" , code="400"}

prometheus_http_requests_total{handler=~"/api.*" , code="200"}

sum ( prometheus_http_requests_total{handler=~"/api.*" , code="200"} )

sort (prometheus_http_requests_total{handler=~"/api.*" , code="200"}  )

sort_desc (prometheus_http_requests_total{handler=~"/api.*" , code="200"}  )

topk(  3,   sort_desc(prometheus_http_requests_total{handler=~"/api.*" , code="200"}  )   )  

bottomk (  3,   sort_desc(prometheus_http_requests_total{handler=~"/api.*" , code="200"}  )   )  

node_memory_MemFree_bytes / 1024 / 1024

node_cpu_seconds_total{mode="idle"} > 4800

node_cpu_seconds_total{mode="idle"} or  node_cpu_seconds_total{mode="iowait"} 


sum (prometheus_http_requests_total ) by (code)

sum (node_cpu_seconds_total)  by (env, mode)

max ( sum (node_cpu_seconds_total)  by (env, mode) )

## About the rate():-
<img width="790" height="241" alt="{632F0901-4138-4FD6-98A1-88A3CE2B21BA}" src="https://github.com/user-attachments/assets/ad746d93-ecf5-4731-846c-a3a9a4cb2a5b" />
<img width="322" height="429" alt="{201A78A9-A7C2-4846-8286-10C1C49D141A}" src="https://github.com/user-attachments/assets/4cf578f0-4daf-4057-a2d3-8870f3686da8" />
<img width="827" height="410" alt="{2CB90E4F-73CC-4771-8508-1772C52F692C}" src="https://github.com/user-attachments/assets/9b77fea3-dea4-4dbd-8d15-f461f92621f2" />
<img width="808" height="351" alt="{2634275E-FC39-471E-8634-DF332F2492B9}" src="https://github.com/user-attachments/assets/c6e379b4-873a-499a-a199-30727fabfc19" />
<img width="511" height="309" alt="{001096F2-0E20-4201-BE69-7E9B75F6DA88}" src="https://github.com/user-attachments/assets/f4bf1434-05aa-420a-a7b9-6b2f82410abe" />
<img width="779" height="228" alt="{8F2DCF69-E8C9-46EB-8EFA-F79E4D664EDD}" src="https://github.com/user-attachments/assets/a997ff08-027d-4c45-8d76-84ed81cb2075" />


irate ( prometheus_http_requests_total[1m] )     ## instant rate change

## About the change(): -
<img width="804" height="281" alt="{5C024441-0056-448C-9258-E24E06CB3A99}" src="https://github.com/user-attachments/assets/2a5956ac-70cc-4f77-a2a3-69a6d7cb9771" />
<img width="507" height="438" alt="{C1838D69-5A14-4ED1-81E8-B66091D86B0F}" src="https://github.com/user-attachments/assets/deff03bf-9107-4d7f-b3a3-a3b08c7ccc6a" />
<img width="798" height="436" alt="{2FA867D8-7CE2-4D36-87A9-439DC489838A}" src="https://github.com/user-attachments/assets/bfdcd988-e7df-4f39-b6c2-8444f40c28f3" />
<img width="759" height="440" alt="{CBAC911B-1F6C-408C-8B62-F2A942E6A536}" src="https://github.com/user-attachments/assets/041ce4d7-1a06-4e08-9097-90fe743de70a" />
<img width="814" height="437" alt="{0C02B7EC-8E93-49FD-A3E9-85DE78EFD515}" src="https://github.com/user-attachments/assets/7ece0d53-48b2-4e43-b426-7e4dfaae3ee2" />


##About deriv(): -
<img width="779" height="281" alt="{4A9D0B82-0BCD-46A9-BD13-6ED3726F6965}" src="https://github.com/user-attachments/assets/b6a57e30-c746-4209-9f88-c3f88cf8b322" />
<img width="543" height="350" alt="{279832B3-C6BD-4F88-9ED5-0D9C2A8881BF}" src="https://github.com/user-attachments/assets/7e7b2540-3551-4655-9623-00a9740d3fb4" />
<img width="799" height="439" alt="{493621BF-0736-4530-BDB9-00C20379BC76}" src="https://github.com/user-attachments/assets/d222acf3-0ca5-4193-a5c2-012dd8da1ea9" />
<img width="699" height="440" alt="{0E42BB01-577A-4C8B-936E-2D41B6B701B8}" src="https://github.com/user-attachments/assets/19e16e90-6c04-45ec-820d-32aa0886c0e3" />
<img width="750" height="391" alt="{A58A4BD4-B492-4A50-9FE9-23F0384548EF}" src="https://github.com/user-attachments/assets/6ae8a909-a305-4fad-ab39-42dd3a3a0831" />
<img width="737" height="306" alt="{D796C348-5D65-49AF-AB45-6949A40D2CBB}" src="https://github.com/user-attachments/assets/5aec6ca6-f20f-4993-bf53-3543cbcb8e40" />

deriv ( process_resident_memory_bytes{job="linuxnode2"}[1h] )   ## resident_memeory => actual used ram.

## About the 2 most important fundamental metric types: -
<img width="782" height="432" alt="{F572306B-CE11-4625-BE53-B0C81E935EEB}" src="https://github.com/user-attachments/assets/02851791-c0ac-48ae-8f2f-e182830d8b4b" />
<img width="670" height="368" alt="{607C29D8-6C3E-44CD-9C47-B510F995495E}" src="https://github.com/user-attachments/assets/3067d724-0eb9-437c-855d-4d6038398688" />
<img width="713" height="320" alt="{2324048B-93E5-4835-A4B6-40C8E00FE6FC}" src="https://github.com/user-attachments/assets/75361e02-b05a-47b4-8d75-f80ffbccb526" />

predict_linear ( node_memory_MemFree_bytes{job="linuxnode1"}[1h]  ,   1 * 60 * 60  * 24)  / 1024 / 1024

( time()  - process_start_time_seconds{job="linuxnode1"}  ) / 60 / 60



