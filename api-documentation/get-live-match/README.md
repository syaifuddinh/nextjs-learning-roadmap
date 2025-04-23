📡 LXSCORE - Get Live Matches API
Retrieve a list of live matches with tournament and team details.

Endpoint
GET /api/match/live?timezone=7

Base URL
https://staging.lxscore.com


🔐 Authorization
This endpoint requires a Bearer Token. Just attach access token as defined below
Access Token:
e7ac2c110f7acdb732c21b94eaa6e9cf802f8e0fc74c2df875d4d3b8fbdcd4a0

Header Example:
Authorization: Bearer e7ac2c110f7acdb732c21b94eaa6e9cf802f8e0fc74c2df875d4d3b8fbdcd4a0


🔧 Query Parameters
Name
Type
Required
Description
timezone
int
Yes
Timezone offset in hours (e.g., 7 for GMT+7)








📥 Sample Request
GET /api/match/live?timezone=7 HTTP/1.1
Host: lxscore.com
Authorization: Bearer e7ac2c110f7acdb732c21b94eaa6e9cf802f8e0fc74c2df875d4d3b8fbdcd4a0


📤 Response
Status: 200 OK
{
  "success": true,
  "data": [
    {
      "id": 4520619,
      "name": "Swansea City-Plymouth Argyle",
      "tournament": {
        "name": "Championship",
        "image": "https://staging.greenscore.id/api/match/images/18785"
      },
      "start_at": "2025-04-09 18:45:00",
      "venue": "Swansea.com Stadium",
      "home_team": {
        "name": "Swansea City",
        "logo": "https://staging.greenscore.id/api/match/images/25091"
      },
      "away_team": {
        "name": "Plymouth Argyle",
        "logo": "https://staging.greenscore.id/api/match/images/25091"
      }
    }
  ]
}



📝 Notes
The start_at field is in server time (adjusted based on the timezone query param).



Ensure the access token is valid; otherwise, you may receive a 401 Unauthorized error.

