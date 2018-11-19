# LINE-BOT-PHP-Starter
<?php
require "vendor/autoload.php";
$access_token = 'Y4YeOUlBvpNZ2AM/4bpPrhs3X+TBiCWtiv3i35X4/RD1ZYHKLiaAftNzD0tJsji451UT+1ha6K1/TBnbPRf9xquw3gvNFVszyNN+ceWkmVTLLMfwb/49jQzzMRbftmXkd1qGjwBvejV74lhOXHDd5QdB04t89/1O/w1cDnyilFU=';
$channelSecret = 'c47b90199b68a57e9bd9144bce45a83f';
$idPush = 'Udfa69d525e239619ccda47d7c8605b57'
$httpClient = new \LINE\LINEBot\HTTPClient\CurlHTTPClient($access_token);
$bot = new \LINE\LINEBot($httpClient, ['channelSecret' => $channelSecret]);
$textMessageBuilder = new \LINE\LINEBot\MessageBuilder\TextMessageBuilder('hello world');
$response = $bot->pushMessage($idPush, $textMessageBuilder);

echo $response->getHTTPStatus() . ' ' . $response->getRawBody();
