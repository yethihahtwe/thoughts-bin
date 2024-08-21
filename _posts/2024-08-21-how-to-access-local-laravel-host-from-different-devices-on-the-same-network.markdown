---
layout: post
title: "How to Access Local Laravel Host from Different Devices on the Same Network"
date: 2024-08-21 04:00:00 +0700
categories: laravel  
---
What can we do when we want to access our locally hosted laravel website from different devices sharing the same WiFi network? We should be able to access our web app or website hosted locally from another device so that we don't have to switch between our IDE and the browser back and forth. That is going to save us a lot of time.

## 1. npm run dev
![NPM](../../../../assets/images/01-laravel-host/01-npm.png)

That is what we normally do `npm run dev`, nothing fancy yet.
## 2. php artisan serve
![new terminal](../../../../assets/images/01-laravel-host/02-new-terminal.png)

Open a new terminal by clicking the `+` icon button. Type the following command:
```
php artisan serve --host=0.0.0.0 --port=8000
```
![PHP](../../../../assets/images/01-laravel-host/03-php-artisan-serve.png)

This is to add the `--host` and `--port` after the usual `php artisan serve` command. Then you'll see your project is hosted.

![server running](../../../../assets/images/01-laravel-host/04-server-running.png)
## 3. Check IP Address
Next thing is to find the ip address of the device where your project is hosted. You can skip this step if you've already known the ip address of your device.

Open a new terminal.

If you're using Linux, type:
```
ip -c a
```
If you're on Windows, type:
```
ipconfig
```
I'm currently on an Ubuntu Linux, then running `ip -c a` will highlight the ip address as you can see in the screenshot.

![Check IP](../../../../assets/images/01-laravel-host/05-check-ip.png)
## 4. Access from another device
On another device sharing the same network, open the browser and in the address bar, enter the ip address of the device where your project is hosted, including the port.

In this example, I'm going type `192.168.1.191:8000` and here's the homepage.

![Device Screen](../../../../assets/images/01-laravel-host/06-access-from-other-device.png)

Thanks for reading. And I'll see you soon. Please leave a comment, if you have any, by sending [email](mailto:yethihahtwe319@gmail.com). 



