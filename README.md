# githubactions_demo

#A workflow run is made up of one or more jobs. Jobs run in parallel by default.

- Trigger the workflow on push or pull request you can choose whatever you want

    on: [push,pull_request]

- The type of machine to run the job on. [Windows,macOS, Ubuntu, self-hosted]

    runs-on: macos-latest
    
-Identifies any jobs that must complete successfully before this job will run.

    needs: test
    
-sequence of tasks called

    steps:
    
- Check out the code from the repository
  
    uses: actions/checkout@v1

- Setup a flutter environment.

      - uses: subosito/flutter-action@v1
        with:
          flutter-version: '1.12.14'
          channel: 'dev'
      - run: flutter pub get

- run static analys code
 
       run: flutter  analyze
       
 -if conditional to prevent a job from running
 
    if: github.event_name != 'pull_request'
       

