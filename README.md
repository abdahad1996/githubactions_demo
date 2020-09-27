<<<<<<< HEAD
# githubactions_demo

#A workflow run is made up of one or more jobs. Jobs run in parallel by default.

-Trigger the workflow on push or pull request you can choose whatever you want

    on: [push,pull_request]

-The type of machine to run the job on. [Windows,macOS, Ubuntu, self-hosted]

    runs-on: macos-latest
    
-Identifies any jobs that must complete successfully before this job will run.

    needs: test
    
-sequence of tasks called

    steps:
    
-Check out the code from the repository
  
    uses: actions/checkout@v1

-Setup a flutter environment.

      - uses: subosito/flutter-action@v1
        with:
          flutter-version: '1.12.14'
          channel: 'dev'
      - run: flutter pub get

-run static analys code
 
       run: flutter  analyze
       
 -if conditional to prevent a job from running
 
    if: github.event_name != 'pull_request'
       

=======
# github_Actions

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
>>>>>>> test
