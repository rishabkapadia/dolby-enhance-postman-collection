# Postman Collection for Dolby Media Enhance API

Jump start exploring Dolby Media Enhance API using this postman collection to improve your audio files like reducing background noise, improving speech quality and much more. This collection will save you a lot of time of manually setting up each request.

## Dynamic Requests 

Data & Request URL required for reuqests are dynamically set via collection variables.

## Setup

1. Sign up for account [here](https://dolby.io)
2. Get API_KEY, API_SECRET
3. Go to Collection -> Add Credentails in Postman Collection variables & confirm other variable values (Sensible defaults have been set)
4. Click 'settings' gear icon on top right -> Settings
5. Scroll down to 'Working Directory' section -> Note the file path
6. Close the window and Paste a audio file (.mp3) in that directory
7. Open 'Upload file via pre-signed URL' request on left pane
8. Click 'Select File' under 'Body' tab and select the .mp3 file

## Set Variable Values

1. audio file (manual input as explained above)
2. input file path - input_file_path
3. output file path - output_file_path
4. retry duration for polling job result (seconds) - polling_retry_duration

## Collection Runner

1. Click Collection on left panel
2. Click Run on top right under Enviornment selection dropdown
3. Untick last 3 Requests
4. Open the 'Console' on bottom left, to see debug info.
5. Click 'Run' on Right pane (big orange button). 
6. Once the process is done, go to 'Download via pre-signed URL' request and click 'Send' request.
7. Playable embeded audio file will be visible in the response pane. 
8. Click 'Save Response' -> Click 'Save to a file'

## Job Result Polling

Once you 'Run' the collection, at 'Check Progress Status' request, it will keep polling every 10 seconds (for a total minimum of 30 seconds) and prints the result so you don't have to manually call the endpoint to check it. NOTE: Sometimes it takes more than 30 seconds for the job to change it's status from Pending to Running. In such cases you will need to update the collection variable 'polling_retries' to 4 (meaning it will poll for 4 times - taking 40 seconds instead of default 3 times taking 30 seconds).

## Documentation

For in-depth usage details like fine tuning the audio processing, please take a look at the [official documentation](https://docs.dolby.io/media-apis/docs/enhance-api-guide).

## Credits

- [Aaron Francis](https://twitter.com/aarondfrancis) - Inspired by his work.
- [Rishab Kapadia](https://twitter.com/rishabkapadia)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
