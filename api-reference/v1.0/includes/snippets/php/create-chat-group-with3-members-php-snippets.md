---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Chat();
$requestBody->setChatType(new ChatType('group'));

$requestBody->setTopic('Group chat title');

$membersConversationMember1 = new AadUserConversationMember();
$membersConversationMember1->setOdataType('#microsoft.graph.aadUserConversationMember');

$membersConversationMember1->setRoles(['owner', 	]);

$additionalData = [
		'user@odata.bind' => 'https://graph.microsoft.com/v1.0/users(\'8c0a1a67-50ce-4114-bb6c-da9c5dbcf6ca\')', 
];
$membersConversationMember1->setAdditionalData($additionalData);



$membersArray []= $membersConversationMember1;
$membersConversationMember2 = new AadUserConversationMember();
$membersConversationMember2->setOdataType('#microsoft.graph.aadUserConversationMember');

$membersConversationMember2->setRoles(['owner', 	]);

$additionalData = [
		'user@odata.bind' => 'https://graph.microsoft.com/v1.0/users(\'82fe7758-5bb3-4f0d-a43f-e555fd399c6f\')', 
];
$membersConversationMember2->setAdditionalData($additionalData);



$membersArray []= $membersConversationMember2;
$membersConversationMember3 = new AadUserConversationMember();
$membersConversationMember3->setOdataType('#microsoft.graph.aadUserConversationMember');

$membersConversationMember3->setRoles(['owner', 	]);

$additionalData = [
		'user@odata.bind' => 'https://graph.microsoft.com/v1.0/users(\'3626a173-f2bc-4883-bcf7-01514c3bfb82\')', 
];
$membersConversationMember3->setAdditionalData($additionalData);



$membersArray []= $membersConversationMember3;
$requestBody->setMembers($membersArray);




$result = $graphServiceClient->chats()->post($requestBody);


```