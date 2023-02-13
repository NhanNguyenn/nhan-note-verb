
| No. | Content                                                               |
| --- | --------------------------------------------------------------------- |
|     |                                                                       |
| 0   | [Shopify-Verb Intergrations APIs](#shopify-verb-intergrations-api)    |
| 1   | [Event API](#event-api)    |
| 2   | [Message Event](#message-event)    |


> Note that the api below is only for ```staging```

# Shopify Verb intergrations API

## Get shopify shop configuration

Using the configuration here to create the payload for ```GetProducts Request```

> https://1hedxmdsmd.execute-api.us-east-1.amazonaws.com/staging/stream/authenticate

    curl 'https://1hedxmdsmd.execute-api.us-east-1.amazonaws.com/staging/stream/authenticate' \
    -H 'authority: 1hedxmdsmd.execute-api.us-east-1.amazonaws.com' \
    -H 'accept: application/json, text/plain, */*' \
    -H 'accept-language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7' \
    -H 'cache-control: no-cache' \
    -H 'origin: https://live-staging.verb.tech' \
    -H 'pragma: no-cache' \
    -H 'referer: https://live-staging.verb.tech/' \
    -H 'sec-ch-ua: "Not?A_Brand";v="8", "Chromium";v="108", "Microsoft Edge";v="108"' \
    -H 'sec-ch-ua-mobile: ?0' \
    -H 'sec-ch-ua-platform: "Windows"' \
    -H 'sec-fetch-dest: empty' \
    -H 'sec-fetch-mode: cors' \
    -H 'sec-fetch-site: cross-site' \
    -H 'user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/108.0.0.0 Safari/537.36 Edg/108.0.1462.54' \
    -H 'x-api-key: IHa5vMmPDW5ueCaqqfzfX6IfcjZSfEvf5PTsByUp' \
    -H 'x-auth-token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE2NzMxMDkyMjMsImVtYWlsIjoibmhhbkBnbWFpbC5jb20iLCJpc3N1ZXJfbWV0YWRhdGEiOnsid2ViaG9va19kb21haW4iOiJodHRwczpcL1wvYmV5b25kc2xpbWFwcC5jb20uYmV0YS5jcm0udmVyYi50ZWNoIiwid2ViaG9va19lbmRwb2ludF9qb2luIjoiaHR0cHM6XC9cL2JleW9uZHNsaW1hcHAuY29tLmJldGEuY3JtLnZlcmIudGVjaFwvcmVtb3RlXC9jb250YWN0c1wvYWRkLmpzb24iLCJ3ZWJob29rX2dyb3VwIjoicmVwc2l0ZXMiLCJ3ZWJob29rX3Rva2VuIjoiZXlKMGVYQWlPaUpLVjFRaUxDSmhiR2NpT2lKSVV6STFOaUo5LmV5SmxlSEFpT2pFMk56TXpOakV5TWpNc0ltbGtJam9pT1RNMU5EazJJaXdpYzJsMFpWOXBaQ0k2SWpFNU9DSjkuVEJvQmNJOEdOZ0hxbnZDMHY0c2UtbjNaSWwyTGkxUFhkWHFpblo3REZHMCIsInNob3Bfc2l0ZV9uYW1lIjoibmhhbiJ9LCJmYW1pbHlfbmFtZSI6IlRoYW5oIiwiZ2l2ZW5fbmFtZSI6Ik5oYW4iLCJuaWNrbmFtZSI6Ik5oYW4gVGhhbmgiLCJ0aGlyZF9wYXJ0eV91c2VybmFtZSI6bnVsbCwiZGlzcGxheV9sYW5ndWFnZSI6ImVuX1VTIiwibG9jYWxlIjoiZW5fVVMiLCJ1c2VyX2xocCI6MCwic3ViIjoicmVwc2l0ZXN8YmV5b25kc2xpbS05MzU0OTYiLCJtYXhfcHJlc2VudGVycyI6bnVsbCwibWF4X251bWJlcl9hdHRlbmRlZXMiOjE1LCJsaXZlX21heF9saXZlX3ZpZGVvcyI6MjUsIm1heF9tZWV0aW5nX2xlbmd0aCI6NjAsInVwZGF0ZWRfYXQiOiIyMDIzLTAxLTA3IDA3OjMzOjQzIiwic3RvcmVfdXJsIjoiaHR0cHM6XC9cL3ZlcmItYmV5b25kc2xpbS1jcm0ubXlzaG9waWZ5LmNvbSIsInN0b3JlX2FwaV9rZXkiOiI2NWI5ZDI4NTFkZDk0MzViZmNlYjdkYTg3MWU2ZTlkNSIsInN0b3JlX3R5cGUiOiJzaG9waWZ5IiwibGl2ZV92aWRlb3MiOmZhbHNlLCJyZWdpb24iOiJhbWVyaWNhIn0.ALyWsbQkE2K-1CoonPaqODYlclmQeBh-bkrKPkwwGY8' \
    --compressed

Expected reponse

    {
        "publicUserData": {
            "close_the_loop": {},
            "display_language": "en_US",
            "email": "nhan@gmail.com",
            "family_name": "Thanh",
            "given_name": "Nhan",
            "issuer_metadata": {
                "webhook_domain": "https://beyondslimapp.com.beta.crm.verb.tech",
                "webhook_endpoint_join": "https://beyondslimapp.com.beta.crm.verb.tech/remote/contacts/add.json",
                "webhook_group": "repsites",
                "webhook_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE2NzMxNDcwODksImlkIjoiOTM1NDk2Iiwic2l0ZV9pZCI6IjE5OCJ9.yXBPo9AEL6DFJp6v7QSCZKtoqL87RAqhHoKfmTjA4L0",
                "shop_site_name": "nhan"
            },
            "live_videos": false,
            "locale": "en_US",
            "nickname": "Nhan Thanh",
            "picture": "",
            "region": "america",
            "store_api_key": "65b9d2851dd9435bfceb7da871e6e9d5",
            "store_type": "shopify",
            "store_url": "https://verb-beyondslim-crm.myshopify.com",
            "sub": "repsites|beyondslim-935496",
            "third_party_username": null,
            "updated_at": "Wed, 04 Jan 2023 20:04:49 GMT",
            "user_lhp": 0,
            "clientId": "repsites",
            "userId": "beyondslim-935496"
        },
        "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE2NzI4OTUwODksImVtYWlsIjoibmhhbkBnbWFpbC5jb20iLCJpc3N1ZXJfbWV0YWRhdGEiOnsid2ViaG9va19kb21haW4iOiJodHRwczpcL1wvYmV5b25kc2xpbWFwcC5jb20uYmV0YS5jcm0udmVyYi50ZWNoIiwid2ViaG9va19lbmRwb2ludF9qb2luIjoiaHR0cHM6XC9cL2JleW9uZHNsaW1hcHAuY29tLmJldGEuY3JtLnZlcmIudGVjaFwvcmVtb3RlXC9jb250YWN0c1wvYWRkLmpzb24iLCJ3ZWJob29rX2dyb3VwIjoicmVwc2l0ZXMiLCJ3ZWJob29rX3Rva2VuIjoiZXlKMGVYQWlPaUpLVjFRaUxDSmhiR2NpT2lKSVV6STFOaUo5LmV5SmxlSEFpT2pFMk56TXhORGN3T0Rrc0ltbGtJam9pT1RNMU5EazJJaXdpYzJsMFpWOXBaQ0k2SWpFNU9DSjkueVhCUG85QUVMNkRGSnA2djdRU0NaS3RvcUw4N1JBcWhIb0tmbVRqQTRMMCIsInNob3Bfc2l0ZV9uYW1lIjoibmhhbiJ9LCJmYW1pbHlfbmFtZSI6IlRoYW5oIiwiZ2l2ZW5fbmFtZSI6Ik5oYW4iLCJuaWNrbmFtZSI6Ik5oYW4gVGhhbmgiLCJ0aGlyZF9wYXJ0eV91c2VybmFtZSI6bnVsbCwiZGlzcGxheV9sYW5ndWFnZSI6ImVuX1VTIiwibG9jYWxlIjoiZW5fVVMiLCJ1c2VyX2xocCI6MCwic3ViIjoicmVwc2l0ZXN8YmV5b25kc2xpbS05MzU0OTYiLCJtYXhfcHJlc2VudGVycyI6bnVsbCwibWF4X251bWJlcl9hdHRlbmRlZXMiOjE1LCJsaXZlX21heF9saXZlX3ZpZGVvcyI6MjUsIm1heF9tZWV0aW5nX2xlbmd0aCI6NjAsInVwZGF0ZWRfYXQiOiIyMDIzLTAxLTA0IDIwOjA0OjQ5Iiwic3RvcmVfdXJsIjoiaHR0cHM6XC9cL3ZlcmItYmV5b25kc2xpbS1jcm0ubXlzaG9waWZ5LmNvbSIsInN0b3JlX2FwaV9rZXkiOiI2NWI5ZDI4NTFkZDk0MzViZmNlYjdkYTg3MWU2ZTlkNSIsInN0b3JlX3R5cGUiOiJzaG9waWZ5IiwibGl2ZV92aWRlb3MiOmZhbHNlLCJyZWdpb24iOiJhbWVyaWNhIn0.Jz1KG11TYxk1H633TvVNGHIMsx8ckzaKyZ0ETSu12h4"
    }

## Get all products

> https://staging-api.verb.tech/products

    curl 'https://staging-api.verb.tech/products' \
    -H 'Accept: application/json, text/plain, */*' \
    -H 'Accept-Language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7' \
    -H 'Connection: keep-alive' \
    -H 'Content-Type: application/json' \
    -H 'Origin: https://live-staging.verb.tech' \
    -H 'Referer: https://live-staging.verb.tech/' \
    -H 'Sec-Fetch-Dest: empty' \
    -H 'Sec-Fetch-Mode: cors' \
    -H 'Sec-Fetch-Site: same-site' \
    -H 'User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/108.0.0.0 Safari/537.36 Edg/108.0.1462.54' \
    -H 'sec-ch-ua: "Not?A_Brand";v="8", "Chromium";v="108", "Microsoft Edge";v="108"' \
    -H 'sec-ch-ua-mobile: ?0' \
    -H 'sec-ch-ua-platform: "Windows"' \
    --data-raw '{"site_id":"","store_url":"https://verb-beyondslim-crm.myshopify.com","store_api_key":"65b9d2851dd9435bfceb7da871e6e9d5","store_type":"shopify","query":"","tag":"","last_item":"","shop_site_name":""}' \
    --compressed

Expected Reponse

    {
        "products": [
            {
                "id": "Z2lkOi8vc2hvcGlmeS9Qcm9kdWN0Lzc4MzUwNjY1OTc2MTc=",
                "cursor": "eyJsYXN0X2lkIjo3ODM1MDY2NTk3NjE3LCJsYXN0X3ZhbHVlIjoiNzgzNTA2NjU5NzYxNyJ9",
                "sku": "ZIP1000",
                "price": "69.95",
                "title": "ZipSlim Charged (30ct)",
                "description": "Lose 3x More Weigh Than With Dieting Alone* ZipSlim® is the delicious way to lose 3X more weight, reduce cravings, and help you become Fitter, Healthier and Happier!+ Enjoy ZipSlim™ Charged 1 hour before a meal and experience a smooth surge of energy thank s to 100mg of natural caffeine extracted from Green Tea. Support Healthy Weight Loss+ Improve Energy Levels+ Control Stress - Induced Cravings+ Why You'll Love ZipSlim® Simple Mix ZipSlim® in 12 - 20oz. of water in seconds, and enjoy! Quality No artificial colors, flavo rs, sweeteners or preservatives Gluten Free Dairy Free Non - GMO Vegetarian Friendly Keto and Paleo friendly Tasty Delicious and refreshing Blackberry Lemonade flavor And IT WORKS~! Enjoy it twice a day – before your 2 largest meals .section { clear: both; padding - top: 40px; border - top: 1px solid #EDEFF6; }",
                "image_url": "https://cdn.shopify.com/s/files/1/0655/2020/6065/products/ZIP1000_x1000.png?v=1666722367",
                "workable_purchase_link": "https://zipslim.info/company/",
                "variable_purchase_link": "https://zipslim.info/{{shop_site_name}}",
                "currency_code": "",
                "currency_symbol": ""
            },
        ],
        "more_products": false
    }

## Filter mechanism

    Filter products by changing the ```payload``` of the ```GetProducts``` api


    {
    "site_id": "",
    "store_url": "https://verb-beyondslim-crm.myshopify.com",
    "store_api_key": "65b9d2851dd9435bfceb7da871e6e9d5",
    "store_type": "shopify",
    "query": "filterString",
    "tag": "Pack",
    "last_item": "",
    "shop_site_name": ""
    }

## Get Product tag/category

> https://staging-api.verb.tech/tags

    curl 'https://staging-api.verb.tech/tags' \
    -H 'Accept: application/json, text/plain, */*' \
    -H 'Accept-Language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7' \
    -H 'Connection: keep-alive' \
    -H 'Content-Type: application/json' \
    -H 'Origin: https://live-staging.verb.tech' \
    -H 'Referer: https://live-staging.verb.tech/' \
    -H 'Sec-Fetch-Dest: empty' \
    -H 'Sec-Fetch-Mode: cors' \
    -H 'Sec-Fetch-Site: same-site' \
    -H 'User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/108.0.0.0 Safari/537.36 Edg/108.0.1462.54' \
    -H 'sec-ch-ua: "Not?A_Brand";v="8", "Chromium";v="108", "Microsoft Edge";v="108"' \
    -H 'sec-ch-ua-mobile: ?0' \
    -H 'sec-ch-ua-platform: "Windows"' \
    --data-raw '{"site_id":"","store_url":"https://verb-beyondslim-crm.myshopify.com","store_api_key":"65b9d2851dd9435bfceb7da871e6e9d5","store_type":"shopify"}' \
    --compressed

Expected Reponse

    [
        "Bundle",
        "Caffeine",
        "Caffeine Free",
        "Charged",
        "Pack",
        "Weight Loss",
        "ZipSlim"
    ]

# Event API

## Store Events - storeEvents

    http:
        path: /events
        method: post

> https://1hedxmdsmd.execute-api.us-east-1.amazonaws.com/staging/events

    curl 'https://1hedxmdsmd.execute-api.us-east-1.amazonaws.com/staging/events' \
    -H 'authority: 1hedxmdsmd.execute-api.us-east-1.amazonaws.com' \
    -H 'accept: application/json, text/plain, */*' \
    -H 'accept-language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7' \
    -H 'content-type: application/json' \
    -H 'origin: https://verblive-staging.shop.com' \
    -H 'referer: https://verblive-staging.shop.com/' \
    -H 'sec-ch-ua: "Not_A Brand";v="99", "Microsoft Edge";v="109", "Chromium";v="109"' \
    -H 'sec-ch-ua-mobile: ?0' \
    -H 'sec-ch-ua-platform: "Windows"' \
    -H 'sec-fetch-dest: empty' \
    -H 'sec-fetch-mode: cors' \
    -H 'sec-fetch-site: cross-site' \
    -H 'user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/109.0.0.0 Safari/537.36 Edg/109.0.1518.52' \
    -H 'x-api-key: IHa5vMmPDW5ueCaqqfzfX6IfcjZSfEvf5PTsByUp' \
    -H 'x-auth-token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE2NzM5NTIyMjgsImVtYWlsIjoibmhhbkBnbWFpbC5jb20iLCJpc3N1ZXJfbWV0YWRhdGEiOnsid2ViaG9va19kb21haW4iOiJodHRwczpcL1wvdW5mcmFuY2hpc2VtYXJrZXRpbmcuY29tLmJldGEuY3JtLnZlcmIudGVjaCIsIndlYmhvb2tfZW5kcG9pbnRfam9pbiI6Imh0dHBzOlwvXC91bmZyYW5jaGlzZW1hcmtldGluZy5jb20uYmV0YS5jcm0udmVyYi50ZWNoXC9yZW1vdGVcL2NvbnRhY3RzXC9hZGQuanNvbiIsIndlYmhvb2tfZ3JvdXAiOiJyZXBzaXRlcyIsIndlYmhvb2tfdG9rZW4iOiJleUowZVhBaU9pSktWMVFpTENKaGJHY2lPaUpJVXpJMU5pSjkuZXlKbGVIQWlPakUyTnpReU1EUXlNamdzSW1sa0lqb2lNVEEzTkRnMU5TSXNJbk5wZEdWZmFXUWlPaUl4TnpraWZRLlNHSzdiUWZtNEs3ZjI0UEJRajhuYUVUdVF0M1BMa3BiMHEycXdXYXhKd0EiLCJzaG9wX3NpdGVfbmFtZSI6ZmFsc2V9LCJmYW1pbHlfbmFtZSI6Ik5ndXllbiBUaGFuaCIsImdpdmVuX25hbWUiOiJOaGFuIiwibmlja25hbWUiOiJOaGFuIE5ndXllbiBUaGFuaCIsInRoaXJkX3BhcnR5X3VzZXJuYW1lIjpudWxsLCJkaXNwbGF5X2xhbmd1YWdlIjoiZW5fVVMiLCJsb2NhbGUiOiJlbl9VUyIsInVzZXJfbGhwIjowLCJzdWIiOiJyZXBzaXRlc3xtYXJrZXRhbWVyLTEwNzQ4NTUiLCJtYXhfcHJlc2VudGVycyI6IjQiLCJtYXhfbnVtYmVyX2F0dGVuZGVlcyI6MTUsImxpdmVfbWF4X2xpdmVfdmlkZW9zIjoyNSwibWF4X21lZXRpbmdfbGVuZ3RoIjo2MCwidXBkYXRlZF9hdCI6IjIwMjMtMDEtMTcgMDE6NDM6NDgiLCJzdG9yZV91cmwiOm51bGwsInN0b3JlX2FwaV9rZXkiOm51bGwsInN0b3JlX3R5cGUiOm51bGwsImxpdmVfdmlkZW9zIjp0cnVlLCJyZWdpb24iOiJhbWVyaWNhIn0.r5dXX_-CLFPpfMEskKbYzCPa5Xwamvq_ljNJD2C29gA' \
    --data-raw '[{"event_data":{"attendee_email":"nhan@gmail.com","attendee_first":"Nhan","attendee_id":"","attendee_role":"","attendee_last":"Nguyen Thanh (host)","client_id":"repsites","stream_id":1100002821,"stream_instance_id":"2aa0563a-515a-4f7b-8571-5f56782eddcb","user_id":"marketamer-1074855","interaction_id":"38508829-441e-4697-8bb5-17940d061985","interaction_label":"Twitter","interaction_action":"https://twitter.com/","interaction_type":"social","interaction_imageUrl":"https://verb-core-configs.s3.amazonaws.com/assets/social.svg","elapsed_seconds":"18","date":"Tue, 17 Jan 2023 08:44:45 GMT"},"event_type":"invite_url_copied","group_parameters":{}}]' \
    --compressed

Expected Reponse

    {
        "message": "OK"
    }

Event type:

    'attendee_left'
    'attendee_limit_reached'
    'attendee_joined'
    'camera_started'
    'camera_stopped'
    'chat_opened'
    'chat_closed'
    'chat_message_sent'
    'guest_sign_in'
    'host_sign_up'
    'invite_url_copied'
    'microphone_enabled'
    'microphone_disabled'
    'screen_share_started'
    'screen_share_stopped'
    'interaction_clicked'
    'interaction_created'
    'stream_started'
    'stream_ended'
    'video_watch_progress'
    'video_created'

---

---

# Message Event

## Message Interface

    export interface RemoteMessageInput {
        action: MessageActions;
        data: DataT;
        type: MessageTypes;
        date?: string;
    }

## Message Action

    export interface MessageActions {
    // chat.*
    'chat.message': string;
    // interaction.*
    'interaction.interaction-data': void;
    // commands.*
    'command': null;
    // stream.*
    'stream.configuration': void;
    }

## Message Types

    export interface MessageTypes {
    // configuration.*
    'configuration.camera-enabled-change': boolean;
    'configuration.options-change': StreamConfigurationResponseSchema;
    'configuration.screen-share-status-change': boolean;
    'configuration.copresenter-join': boolean;
    'configuration.stream-duration': number;
    'configuration.stream-paused': boolean;
    'configuration.stream-start': null;
    'configuration.stream-end': null;
    'configuration.join-data': ConfigurationJoinData;

    // interaction.*
    'interaction.interaction-data': InteractionDataPayload;
    'interaction.clicked': string;
    'interaction.edited': string;

    // command.*
    'presenter.mute': boolean;

    // chat.*
    'chat.message': string;

    // shopping.*
    'shop.enable-shop': boolean;
    'shop.activity': string;
    'shop.update-products': ShopUpdateProductsPayload;
    'shop.owner-change': ShopOwnerChangePayload;
    }

## Sample message

Chat message event:

    {
    "text": {
        "action": "chat.message",
        "data": "hello",
        "type": "chat.message",
        "date": "2023-02-07T09:16:22.301Z"
    },
    "messageType": "TEXT"
    }

Stream duration event (elapsedSeconds):

    {
    "text": {
        "data": {
        "elapsedSeconds": 731,
        },
        "action": "stream.configuration",
        "type": "configuration.join-data"
    },
    "messageType": "TEXT"
    }

Stream start 

    {
    action: "stream.configuration",
    data: null,
    type: "configuration.stream-start",
    }

Stream end

    {
    action: "stream.configuration",
    data: null,
    type: "configuration.stream-end",
    }


# /authentication/referrer

https://1hedxmdsmd.execute-api.us-east-1.amazonaws.com/staging/authentication/referrer

```x-auth-token``` is CRM user token

    curl -X GET \
    'https://1hedxmdsmd.execute-api.us-east-1.amazonaws.com/staging/authentication/referrer' \
    --header 'x-api-key: IHa5vMmPDW5ueCaqqfzfX6IfcjZSfEvf5PTsByUp' \
    --header 'x-auth-token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE2NzYzMDM5NTksImVtYWlsIjoiZHVuZ25ndXllbkBtYWlsaW5hdG9yLmNvbSIsImlzc3Vlcl9tZXRhZGF0YSI6eyJ3ZWJob29rX2RvbWFpbiI6Imh0dHBzOlwvXC91bmZyYW5jaGlzZW1hcmtldGluZy5jb20uYmV0YS5jcm0udmVyYi50ZWNoIiwid2ViaG9va19lbmRwb2ludF9qb2luIjoiaHR0cHM6XC9cL3VuZnJhbmNoaXNlbWFya2V0aW5nLmNvbS5iZXRhLmNybS52ZXJiLnRlY2hcL3JlbW90ZVwvY29udGFjdHNcL2FkZC5qc29uIiwid2ViaG9va19ncm91cCI6InJlcHNpdGVzIiwid2ViaG9va190b2tlbiI6ImV5SjBlWEFpT2lKS1YxUWlMQ0poYkdjaU9pSklVekkxTmlKOS5leUpsZUhBaU9qRTJOelkxTlRVNU5Ua3NJbWxrSWpvaU1UQTNORGcwTmlJc0luTnBkR1ZmYVdRaU9pSXhOemtpZlEuY3JydDZuVkJ5UVlLc0J2NE81eG1XbkZqZ1UtT0JGTGtYSFBmU04za0ttayIsInNob3Bfc2l0ZV9uYW1lIjpmYWxzZX0sImZhbWlseV9uYW1lIjoibmd1eWVuIiwiZ2l2ZW5fbmFtZSI6ImR1bmciLCJjb21wYW55X25hbWUiOiJNYXJrZXQgQW1lcmljYSIsIm5pY2tuYW1lIjoiZHVuZyBuZ3V5ZW4iLCJ0aGlyZF9wYXJ0eV91c2VybmFtZSI6ImR1bmduZ3V5ZW4iLCJkaXNwbGF5X2xhbmd1YWdlIjoiZW5fVVMiLCJsb2NhbGUiOiJlbl9VUyIsInVzZXJfbGhwIjowLCJzdWIiOiJyZXBzaXRlc3xtYXJrZXRhbWVyLTEwNzQ4NDYiLCJtYXhfcHJlc2VudGVycyI6IjQiLCJtYXhfbnVtYmVyX2F0dGVuZGVlcyI6MTUsImxpdmVfbWF4X2xpdmVfdmlkZW9zIjoyNSwibWF4X21lZXRpbmdfbGVuZ3RoIjo2MCwidXBkYXRlZF9hdCI6IjIwMjMtMDItMTMgMDY6NTk6MTkiLCJzdG9yZV91cmwiOm51bGwsInN0b3JlX2FwaV9rZXkiOm51bGwsInN0b3JlX3R5cGUiOm51bGwsImxpdmVfdmlkZW9zIjp0cnVlLCJyZWdpb24iOiJhbWVyaWNhIn0.WOYMKQUEI0AvpBqSn1Kt5MbBlUUk4cdlm2sIzs5l11g'


