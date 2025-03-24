# verus-ccminer
ccminer verus with luckpool and vipor

apk autostart app

    https://github.com/xenon24/verus-ccminer/blob/main/autostart201_A-Signed.apk

    https://drive.google.com/file/d/1TBzfrx1m72BjatU-_gUuWtG6n2Zla-XJ/view?usp=sharing

Download & install latest arm64-v8a

    https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_arm64-v8a.apk

Get Termux ready

    yes | pkg update && pkg upgrade
    yes | pkg install libjansson wget nano

Download ccminer, config, start

    mkdir ccminer && cd ccminer
    wget https://raw.githubusercontent.com/Darktron/pre-compiled/generic/ccminer
    wget https://raw.githubusercontent.com/Darktron/pre-compiled/generic/config.json
    wget https://raw.githubusercontent.com/Darktron/pre-compiled/generic/start.sh
    chmod +x ccminer start.sh

edit nano

    nano config.json

copy program 

    {
          "pools":
            [{
                "name": "NA-LUCKPOO8L",
                "url": "stratum+tcp://ap.luckpool.net:3956",
                "timeout": 180,
                "disabled": 1
            }],

        "user": "RLacyFLRVTwdH8TTuxRBMoru8esamUXP7u.min03",
        "pass": "",
        "algo": "verus",
        "threads": 8,
        "cpu-priority": 1,
        "cpu-affinity": -1,
        "retry-pause": 10,
        "api-allow": "192.168.0.0/16",
        "api-bind": "0.0.0.0:4068"
    }

copy program 1

    {
          "pools":
            [{
                "name": "NA-LUCKPOO8L",
                "url": "stratum+tcp://ap.luckpool.net:3956",
                "timeout": 180,
                "disabled": 1
            }],

        "user": "RLacyFLRVTwdH8TTuxRBMoru8esamUXP7u.kenzo13",
        "pass": "",
        "algo": "verus",
        "threads": 8,
        "cpu-priority": 1,
        "cpu-affinity": -1,
        "retry-pause": 10,
        "api-allow": "192.168.0.0/16",
        "api-bind": "0.0.0.0:4068"
    }

 Vipor

     {
        "pools":
            [{
                "name": "SG-VIPOR",
                "url": "stratum+tcp://sg.vipor.net:5040",
                "timeout": 180,
                "disabled": 0
            }],

        "user": "RLacyFLRVTwdH8TTuxRBMoru8esamUXP7u.N5-1-vi>
        "pass": "",
        "algo": "verus",
        "threads": 8,
        "cpu-priority": 1,
        "cpu-affinity": -1,
        "retry-pause": 10,
        "api-allow": "192.168.0.0/16",
        "api-bind": "0.0.0.0:4068"
    }

start

    ~/ccminer/start.sh

setting auto run

    nano ../usr/etc/bash.bashrc

up code 

    cd ccminer/&&./start.sh
