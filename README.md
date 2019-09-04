Put the service in file: `/lib/systemd/system/oyunkeyf.service`

Service:
    
    [Unit]
    Description=Oyunkeyf Service
    
    [Service]
    Type=simple
    WorkingDirectory=/home/eguneys/oyun
    ExecStart=/home/eguneys/oyun/bin/oyun -Dhttp.port=9000 -Dconfig.file=/home/eguneys/oyun/application.conf -Dplay.crypto.secret="insertsecrethere" 
    Restart=always
    
    [Install]
    WantedBy=multi-user.target
