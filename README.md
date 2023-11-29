<p align="center">
  <img src="https://avatars.githubusercontent.com/u/152215067?s=200&v=4" height="80">
</p>

# LabsMobile-Yii-v2.0

![](https://img.shields.io/badge/version-1.0.0-blue.svg)
 
Send SMS messages through the LabsMobile platform and the Yii Framework. Install the LabsMobile module for Yii and in a few seconds you will be able to send SMS messages.

## Documentation

Labsmobile API documentation can be found [here][apidocs].

## Features
  - Send SMS messages.
  - Check the credits of your LabsMobile account

## Requirements

- Yii 2.0. More info at [Yii Framework][yiiframework].
- A user account with LabsMobile. Click on the link to create an account [here][signUp].

## Installation

1. Copy the LabsMobileSMS folder into /vendor

2. Add the following lines into your configuration file (ex. /config/web.php)

 ```php
...
'components' => [
        ...
        'sms' => [
            'class' => 'app\vendor\LabsMobileSMS\LabsMobileSMS',
            'LMaccount_username'=>'{YOUR USERNAME}',
            'LMaccount_password'=>'{YOUR PASSWORD}',
            'LMaccount_clientapi'=>'{YOUR API CLIENT}',
        ],
  ```

3. Now you can send messages with the following code:
 ```php
   Yii::$app->sms->send(array('to'=>'14158141829', 'message'=>'Hello world!'));
  ```

4. Or check the number of credits available in your account LabsMobile:
  ```php
    <?php ...
    Yii::$app->sms->get_balance();
  ```


## Help

If you have questions, you can contact us through the support chat or through the support email support@labsmobile.com.

[apidocs]: https://www.labsmobile.com/en/api-sms
[signUp]: https://www.labsmobile.com/en/signup
[yiiframework]: https://www.yiiframework.com/