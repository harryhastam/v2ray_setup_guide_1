# v2ray_setup_guide_1
v2ray setup guide - 1

Thanks to the one-command script by 233blog.com, you can install v2ray even if you are not familiar with Linux commands. 

You need to have at least Ubuntu 16, Debian 8 or CentOS 7. 

This guide will be for Ubuntu.

1. First make updates and upgrades

sudo apt-get update

sudo apt-get upgrade

2. Run the v2ray script

bash <(curl -s -L https://git.io/v2ray.sh)

If you run into the error “curl command not found” then run this command:

apt-get update -y && apt-get install curl -y

3. First question will ask you which version you choose. No major differences between 1 and 2. You can choose 1.

4. Next you choose the protocol. For sake of simplicity let’s choose TCP.

5. Now you choose the port. You can choose the default value or change it. I choose port 23432.

23432

6. Then you choose to install an ad-blocker or not. It is noted that performance may be affected if ad-blocker is activated. I choose not to install it.

N

7. You will be asked whether you also want to install Shadowsocks. If you type Y,  then you will have to choose a Shadowsocks port, a password and an encryption method. I will keep it simple and choose not to install Shadowsocks.

N

8. And lastly, you press Enter to proceed or Ctrl+C to cancel. After a while, the setup will be complete. Now you can get v2ray configuration by typing v2ray qr (for QR code) or v2ray link (for url).

Managing  v2ray
V2ray commands
v2ray info – View V2Ray configuration information
v2ray config – Modify V2Ray configuration
v2ray link – Generate V2Ray configuration file link
v2ray infolink – Generate V2Ray configuration information link
v2ray qr – Generate V2Ray configuration QR code link
v2ray ss – Modify Shadowsocks configuration
v2ray ssinfo – View Shadowsocks configuration information
v2ray ssqr – Generate Shadowsocks Configure QR code link
v2ray status – View V2Ray running status
v2ray start – Start V2Ray
v2ray stop – stop V2Ray
v2ray restart – restart V2Ray
v2ray log – View V2Ray Run log
v2ray update – Update V2Ray
v2ray update.sh – update V2Ray management script
v2ray uninstall – Uninstall V2Ray

Adding multiple users on v2ray (Bonus)

The v2ray script adds only one user as a default, you can add multiple users by editing the config file. Normally, you would not need to add multiple users, since multiple users can use the same configuration. I have added this section as a bonus.
1. First, generate multiple UUIDs on the uuidgenerator.net
2. Next, SSH into your VPS and type nano /etc/v2ray/config.json to edit the config file
3. Default configuration of users is given as following:

“users”: [
{
“id”: “b831381d-6324-4d53-ad4f-8cda48b30811”, 
“alterId”: 233
}
]
4. You shoud edit the config as given below, note that I add a comma sign (,)  and copy and paste the above user config in brackets and change the uuid:
“users”: [
{
“id”: “b831381d-6324-4d53-ad4f-8cda48b30811”, 
“alterId”: 233 
},
{
“id”: “z454362o-4324-8b12-gh1l-8zer71r59603”, 
“alterId”: 233
} 
]


5. You can add as many users as you want following the above guide. Just repeat the process. After adding users press Ctrl+X to exit the config, and press Y to save the changes.

Installing v2ray to Your Devices

v2ray apps for Android
You can use v2ray on several apps on Android, and all of them are available for free Google Play.

v2RayNG
Kitsunebi
BifrostV
V2Ray
Clash for Android

v2ray apps for iOS
You can use v2ray on several apps on your iPhone/iPad as well, most of the v2ray apps are paid apps, except for 91VPN.

ShadowRocket
Kitsunebi – supports UDP relay
Quantumult
i2Ray
Pepi
91VPN
Pharos Pro

v2ray clients for Windows
For your Windows PC, you can choose one of these three v2ray Windows clients. And here is a download link. There is also a new software called Clash, that requires a 64-bit Windows. You can download it here.

V2RayW
V2RayN
V2RayS
Clash

v2ray clients for MacOS
For your Mac PC, you can choose one of these two v2ray clients. And here is a download link for V2RayX and here for V2RayU. Click here to download ClashX for MacOS.

V2RayX
V2RayU
ClashX
