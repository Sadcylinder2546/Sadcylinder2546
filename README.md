curl -X POST -H "Content-Type: application/json" -d '{
     "platform": "instagram",
     "ice_breakers":[
       {
          "call_to_actions":[
             {
                "question":"<QUESTION>",
                "payload":"<PAYLOAD>"
             },
             {
                "question":"<QUESTION>",
                "payload":"<PAYLOAD>"
             }
          ],
          "locale":"default" // default locale is REQUIRED
       },
       {
          "call_to_actions":[
             {
                "question":"<QUESTION>",
                "payload":"<PAYLOAD>"
             },
             {
                "question":"<QUESTION>",
                "payload":"<PAYLOAD>"
             }
          ],
          "locale":"en_GB"
       }
    ]
}' "https://graph.facebook.com/v11.0/me/messenger_profile?platform=instagram&access_token=<PAGE_ACCESS_TOKEN>"
Old format (should not be used for new Icebreaker setup)
curl -X POST -H "Content-Type: application/json" -d '{
  "platform": "instagram",
  "ice_breakers":[
     {
        "question": "<QUESTION>",
        "payload": "<PAYLOAD>"
     },
     {
        "question": "<QUESTION>",
        "payload": "<PAYLOAD>"
     },
     ...

  ]
}' "https://graph.facebook.com/v11.0/me/messenger_profile?platform=instagram&access_token=<PAGE_ACCESS_TOKEN>"
