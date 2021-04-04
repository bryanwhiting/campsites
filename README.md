# Campsite availability via CLI

Small tool to check for campsite availability and notify via text message using Twilio.



```
Usage: find-campsites [OPTIONS]

  Search for campsite availability from recreation.gov.

Options:
  -c, --campground TEXT           Name of campground to search for
                                  availability

  -n, --nights INTEGER            Number of nights to stay  [default: 1]
  -d, --day [Sunday|Monday|Tuesday|Wednesday|Thursday|Friday|Saturday]
                                  Weekday of reservation start (can specify
                                  multiple) [default: all days]

  -m, --months INTEGER            Number of months to search  [default: 1]
  --check_every INTEGER           Minutes to wait before checking again
                                  [default: 60]

  --require_same_site             Require campsite to be the same over all
                                  nights (no switching campsites)

  --notify                        Send text message if campsite is available
  --help                          Show this message and exit.
  ```

Text message support can be added by creating a Twilio account and adding the following to either a `.env` file in the project root, or adding to environment variables.

```
TWILIO_ACCOUNT_SID="YOUR_TWILIO_SID"
TWILIO_AUTH_TOKEN="YOUR_TWILIO_AUTH"
TWILIO_FROM_NUMBER="YOUR_TWILIO_NUMBER"
TWILIO_TO_NUMBER = "YOUR_PHONE_NUMBER"
```
