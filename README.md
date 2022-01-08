# google-calender-setup

## set-up
follow the quick start at https://developers.google.com/calendar/api/quickstart/go

## credential key
these code depends on the credential key , which will need to be created on the google cloud platform
1. specfic project
2. create the key
3. in the main tab of Auth, you will see OAuth displays at the right side, there's a icon for downloading it, click it.
4. rename it, for example if running in GOLANG , rename it as credential.json and put it into the same directory as code.

## create a event
1. look into the code , change the code from
```
  config, err := google.ConfigFromJSON(b, calendar.CalendarReadonlyScope)
```
into
```
  config, err := google.ConfigFromJSON(b, calendar.CalendarScope)
```
2. delete the token.json
3. add in the code in https://developers.google.cn/calendar/api/v3/reference/events/insert?hl=zh-cn#go

## Configure access with application
enter : https://console.cloud.google.com/apis/credentials/consent?hl=zh-tw&project=uber-demo-327504
