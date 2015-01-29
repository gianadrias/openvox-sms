
# openvox-sms
OpenVox VoxStack GSM-gateway sms sender


Intro
=====

OpenVox VoxStack GSM-gateway have inside Asterisk PBX (http://www.asterisk.org)
Asterisk have AMI (Asterisk Manager Interface) - telnet connection 
for exchange commands and events


Install
=======

> npm install openvox-sms --save


Usage
=====

`````
var osms = require('openvox-sms');

var sms = new osms({host: 'localhost'});

sms.open(function () {
	sms.sendSMS({span: 1, number: '89135292926', text: 'hello'}, function (response) {
		console.log('Done!');
	});
});

`````

API
===

*sms.sendSMS*

sendSMS({
	span: 1,                  // span of gsm board
	number: '89135292926',    // number 
	text: 'hello'             // text can be long, more than 160 for ascii sms and more than 70 for non-ascii sms
	}, callback);             // callback receive one response for short sms or array for long sms




Bugs?
=====

Please, contact with me


Links
=====

http://habrahabr.ru/post/205122/

http://mysyura.in.ua/otpravka-shlyuz-openvox/

http://www.openvox.cn/pub/manuals/Release/English/VS-GW1600-20G%20User%20Manual.pdf

http://www.openvox.cn/products/voip-gateways/gsm-gateways/148/vs-gw1600-gsm-series-detail.html

http://openvox.qiniudn.com/pub/misc/GSM%20Gateway/OpenVox%20%20GSM%20Gateway%20HTTP%20Interface_en.pdf


