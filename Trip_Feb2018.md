# Trip to SE Asia
**February-March 2018**

```mermaid
gantt
        dateFormat  MM-DD-H:m
        title Flight timing
        section Flights
          SFO - DPS : l1, 02-17-12:05, 02-18-11:35
          DPS - YOG : l2, after bali, 3h
          YOG - KLIA : l3, after yog, 3h
          KLIA - SIN : l4, after kul, 3h
          SIN - SFO : l5, 03-02-15:45, 1d
        section Stays
          Bali : bali, after l1, 5d
          Yogakarta : yog, after l2, 2d
          Kuala Lumpur : kul, after l3, 3d
          Singapore : sin, after l4, 2d
        section Trip
          Trip : active,trip, 02-18-11:35, 03-02-15:45
        section Concerns
          Chinese New Year : crit,cny, 02-16-00:00, 15d
          Chinese New Year Holiday : crit,cnyh, 02-16-00:00, 5d

```

  <!-- - Fly SFO - KLIA ( / )
Kuala Lumpur
  - Fly KLIA - DPS ( $40 )
  - Fly KLIA - YOG ( $60 )
Indonesia
  - Fly within ( $35 )
  - Fly DPS - SIN ( $50 )
  - Fly YOG - SIN ( $100 )
Singapore
  - Fly SIN - SFO ( / )


  - Fly SFO - KLIA ( +$100 )
Bali
  - Fly DPS - KLIA ()
Kuala Lumpur
  - Fly KLIA - KLIA ()
Singapore -->

### Rules
1. Singapore needs to be last (CNY)
2. Don't take train or bus

### Plan 1
```mermaid
graph LR
  SFO>SFO] -- P 0 --> KLIA
  KLIA -- P 60 --> YOG
  YOG -- P 35 --> DPS
  DPS -- P 50 --> SIN
  SIN -- P 0 --> SFO_r
  SFO_r[SFO]
```
\$145
### Plan 2
#### 2a
```mermaid
graph LR
  SFO>SFO] -- P 100? --> DPS
  DPS -- P 35 --> YOG
  YOG -- P 60 --> KLIA
  KLIA -- B 15 / T 35 --> SIN
  SIN -- P 0? --> SFO_r
  SFO_r[SFO]
```
\$210 / \$230
#### 2b
```mermaid
graph LR
  SFO>SFO] -- P 100? --> DPS
  DPS -- P 35 --> YOG
  YOG -- P 60 --> KLIA
  KLIA -- P 30 --> SIN
  SIN -- P 0? --> SFO_r
  SFO_r[SFO]
```
\$205
