jenkins-destop-notify
=====================
Send desktop notifications on jenkins jobs status changes (completion, failure etc)

Works on fedora, ubuntu etc eg. where you able to install ``notify-send``.

Require: notify-send

Run::


        ./jenkins-desktop-notify <path-to-config-file>


Configuration
-------------

Config file is a simple json file::


        {
         "jenkins url" : "<put jenkins url to specific view here, this is only required config option>", 
         "jobs": [<put list of jobs that you want to watch here. Other jobs will be ignored>],
         "user": "<Specify user name here, if your jenkins requres auth for access. You can omit this and password fields if your jenkins doesn't require auth>",
         "password": "Specify Jenkins API token (find it in your jenkins profile) or password (on old jenkins)"
        }


where jenkins url is url pointing to specific view, for example ``http://127.0.0.1:8080/view/All``
