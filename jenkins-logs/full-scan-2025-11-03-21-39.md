# Jenkins Execution Log

## Build Information
- **Job Name:** `MBP_Github_BlackduckSca_Test/main`
- **Build Number:** #44
- **Build Status:** 🔴 **FAILURE**
- **Duration:** 4 min 21 sec and counting
- **Timestamp:** 2025-11-03 21:39:22 UTC

---

## Console Output

```
Started by user admin
Connecting to https://api.github.com using madhusud@blackduck.com/****** (Github_Username_PAT)
Obtained nodejs-npm/Jenkinsfile from cfa583d11977ac6e7afb5d391625795e5ebb9dbc
Loading library blackduck-logs-publisher@main
Attempting to resolve main from remote references...
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git ls-remote -h -- https://github.com/integrations-garage/blackduck-logs-publisher # timeout=10
Found match: refs/heads/main revision 6350ab1192c903b299e4f68d10bf81dd7e189c3c
The recommended git tool is: NONE
using credential Github_Username_PAT
 > git rev-parse --resolve-git-dir /Users/madhusud/.jenkins/workspace/BP_Github_BlackduckSca_Test_main@libs/a0dda568bac7bbb4a171f59ba3f2660c21c69edc6356524e9ae8bb4500c12bbb/.git # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/integrations-garage/blackduck-logs-publisher # timeout=10
Fetching without tags
Fetching upstream changes from https://github.com/integrations-garage/blackduck-logs-publisher
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git fetch --no-tags --force --progress -- https://github.com/integrations-garage/blackduck-logs-publisher +refs/heads/*:refs/remotes/origin/* # timeout=10
Checking out Revision 6350ab1192c903b299e4f68d10bf81dd7e189c3c (main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 6350ab1192c903b299e4f68d10bf81dd7e189c3c # timeout=10
Commit message: "Phase 2"
 > git rev-list --no-walk 6350ab1192c903b299e4f68d10bf81dd7e189c3c # timeout=10
[Pipeline] Start of Pipeline
[Pipeline] node
Running on mac-sh in /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Checkout SCM)
[Pipeline] checkout
The recommended git tool is: NONE
using credential Github_Username_PAT
Fetching changes from the remote Git repository
Fetching without tags
 > git rev-parse --resolve-git-dir /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/.git # timeout=10
 > git config remote.origin.url https://github.com/blackducksca-jenkins-samples/full-scan.git # timeout=10
Fetching upstream changes from https://github.com/blackducksca-jenkins-samples/full-scan.git
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git fetch --no-tags --force --progress -- https://github.com/blackducksca-jenkins-samples/full-scan.git +refs/heads/main:refs/remotes/origin/main # timeout=10
Checking out Revision cfa583d11977ac6e7afb5d391625795e5ebb9dbc (main)
Commit message: "Jenkins log upload - Build #43"
 > git config core.sparsecheckout # timeout=10
 > git checkout -f cfa583d11977ac6e7afb5d391625795e5ebb9dbc # timeout=10
 > git rev-list --no-walk 39e4eacff8d8dc343a929ee5e36ff82196513b8f # timeout=10
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Build)
[Pipeline] script
[Pipeline] {
[Pipeline] echo
JOB_NAME: MBP_Github_BlackduckSca_Test/main
[Pipeline] dir
Running in /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
[Pipeline] {
[Pipeline] sh
+ node --version
v22.16.0
[Pipeline] sh
+ npm --version
10.9.2
[Pipeline] sh
+ npm install
npm warn deprecated fsevents@1.2.9: fsevents 1 will break on node v14+ and could be using insecure binaries. Upgrade to fsevents 2.

up to date in 3m

32 packages are looking for funding
  run `npm fund` for details
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (blackduck-security-scan)
[Pipeline] script
[Pipeline] {
[Pipeline] dir
Running in /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
[Pipeline] {
[Pipeline] echo
DETECT_PROJECT_NAME will be set to: MBP_Github_BlackduckSca_Test
[Pipeline] withEnv
[Pipeline] {
[Pipeline] security_scan
**************************** START EXECUTION OF BLACK DUCK SECURITY SCAN ****************************
[Security Scan] INFO: Jenkins Job name: MBP_Github_BlackduckSca_Test
-------------------------------- Connection to node --------------------------------
[Security Scan] INFO: Jenkins job is running on agent node remotely
-------------------------- Parameter Validation Initiated --------------------------
[Security Scan] INFO:  --- product = [BLACKDUCKSCA]
[Security Scan] INFO: Parameters for blackducksca:
[Security Scan] INFO:  --- blackducksca_waitForScan = true
[Security Scan] INFO:  --- blackducksca_scan_full = true
[Security Scan] INFO:  --- blackducksca_token = ******************************************************************************
[Security Scan] INFO:  --- blackducksca_url = https://saastest.app.blackduck.com
------------------------------------------------------------------------------------
[Security Scan] INFO: Parameters for additional configuration:
[Security Scan] INFO:  --- include_diagnostics = true
[Security Scan] INFO:  --- mark_build_status = FAILURE
[Security Scan] INFO:  --- network_airgap = false
[Security Scan] INFO: Black Duck SCA parameters are validated successfully
[Security Scan] INFO: Bridge download parameters are validated successfully
[Security Scan] INFO: Bridge download is not required. Found installed in: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
------------------------------------------------------------------------------------
[Security Scan] INFO: Bridge CLI version is - 3.9.2
[Security Scan] INFO: Jenkins Job name: MBP_Github_BlackduckSca_Test
[Security Scan] INFO: Jenkins Job name: MBP_Github_BlackduckSca_Test
[Security Scan] INFO: Executable command line arguments: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm/bridge-cli --stage blackducksca --input /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/blackducksca_input1143467569328247248.json --out .bridge/output/scan_info_out.json --diagnostics

******************************* START EXECUTION OF BRIDGE CLI *******************************
2025-11-03 21:38:15.0893 IST [Bridge CLI] INFO: Using cache directory: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
2025-11-03 21:38:15.0998 IST [Bridge CLI] INFO: Found version "3.0.143" in registry for workflow "blackducksca", trying to load it from local cache
2025-11-03 21:38:15.1060 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA Controller
2025-11-03 21:38:15.1062 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA Results
2025-11-03 21:38:15.1064 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA Detect Execution
2025-11-03 21:38:15.1068 IST [Bridge CLI] DEBUG: New adapter loaded: Detect Component Locator
2025-11-03 21:38:15.1070 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA SARIF Issues Fetcher
2025-11-03 21:38:15.1073 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA SARIF Generator
2025-11-03 21:38:15.1075 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA Gitlab Reports Generator
2025-11-03 21:38:15.1076 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA Policy Violations Fetcher
2025-11-03 21:38:15.1188 IST [Bridge CLI] DEBUG: New adapter loaded: Downloader Adapter
2025-11-03 21:38:15.1299 IST [Bridge CLI] DEBUG: New adapter loaded: SCM Checker
2025-11-03 21:38:15.1313 IST [Bridge CLI] DEBUG: New adapter loaded: GitHub Badges
2025-11-03 21:38:15.1454 IST [Bridge CLI] DEBUG: New adapter loaded: GitHub Pull Request Handler
2025-11-03 21:38:15.1454 IST [Bridge CLI] DEBUG: New adapter loaded: GitLab Pull Request Handler
2025-11-03 21:38:15.1455 IST [Bridge CLI] DEBUG: New adapter loaded: Azure Pull Request Handler
2025-11-03 21:38:15.1455 IST [Bridge CLI] DEBUG: New adapter loaded: Bitbucket Pull Request Handler
2025-11-03 21:38:15.1582 IST [Bridge CLI] DEBUG: New adapter loaded: GitHub Commenter
2025-11-03 21:38:15.1583 IST [Bridge CLI] DEBUG: New adapter loaded: Gitlab Commenter
2025-11-03 21:38:15.1583 IST [Bridge CLI] DEBUG: New adapter loaded: Azure Commenter
2025-11-03 21:38:15.1583 IST [Bridge CLI] DEBUG: New adapter loaded: Bitbucket Commenter
2025-11-03 21:38:15.1759 IST [Bridge CLI] DEBUG: New adapter loaded: Detect Installer
2025-11-03 21:38:15.2143 IST [Bridge CLI] INFO: Input Resources:
2025-11-03 21:38:15.2144 IST [Bridge CLI] INFO: resource = value [source]
2025-11-03 21:38:15.2144 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-03 21:38:15.2144 IST [Bridge CLI] INFO: blackducksca.scan.full = true [blackducksca_input1143467569328247248.json]
2025-11-03 21:38:15.2144 IST [Bridge CLI] INFO: blackducksca.token = ***************************************** [blackducksca_input1143467569328247248.json]
2025-11-03 21:38:15.2144 IST [Bridge CLI] INFO: blackducksca.url = https://saastest.app.blackduck.com [blackducksca_input1143467569328247248.json]
2025-11-03 21:38:15.2144 IST [Bridge CLI] INFO: blackducksca.waitForScan = true [blackducksca_input1143467569328247248.json]
2025-11-03 21:38:15.2144 IST [Bridge CLI] INFO: network.airgap = false [blackducksca_input1143467569328247248.json]
2025-11-03 21:38:15.2144 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-03 21:38:15.2144 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca
2025-11-03 21:38:15.2147 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Controller
2025-11-03 21:38:15.2220 IST [Bridge CLI] DEBUG: New adapter loaded: Check pull request
2025-11-03 21:38:15.2221 IST [Bridge CLI] INFO: Starting Adapter: Check pull request
2025-11-03 21:38:15.2533 IST [Check pull request] INFO: Provided value for resource 'environment.scan.pull'
2025-11-03 21:38:15.2533 IST [Check pull request] DEBUG: Provided value 'false' for resource 'environment.scan.pull'
2025-11-03 21:38:15.2535 IST [Check pull request] INFO: Adapter finished
2025-11-03 21:38:16.2893 IST [Blackduck SCA Controller] INFO: Found Black Duck SCA Detect jar file "detect-11.0.0.jar" in "/Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0"
2025-11-03 21:38:16.3068 IST [Blackduck SCA Controller] INFO: Provided value for resource 'detect.execution.path'
2025-11-03 21:38:16.3069 IST [Blackduck SCA Controller] DEBUG: Provided value '/Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0/detect-11.0.0.jar' for resource 'detect.execution.path'
2025-11-03 21:38:16.3069 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-detect
2025-11-03 21:38:16.3069 IST [Bridge CLI] INFO: Starting adapters for stage scm
2025-11-03 21:38:16.3069 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-post-processing
2025-11-03 21:38:16.3082 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Results
2025-11-03 21:38:16.3083 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Detect Execution
2025-11-03 21:38:16.3083 IST [Bridge CLI] INFO: Starting Adapter: SCM Checker
2025-11-03 21:38:16.3083 IST [Bridge CLI] INFO: Starting Adapter: Detect Component Locator
2025-11-03 21:38:16.3091 IST [Blackduck SCA Controller] INFO: Adapter finished
2025-11-03 21:38:16.3967 IST [Blackduck SCA Detect Execution] INFO: Running command /Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home/bin/java -jar /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0/detect-11.0.0.jar --detect.cleanup=false --detect.bdio.file.name=scan --detect.bdio.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact --detect.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect --detect.diagnostic=true --blackduck.offline.mode=false --blackduck.url=https://saastest.app.blackduck.com --blackduck.api.token= --detect.wait.for.results=true --detect.blackduck.scan.mode=INTELLIGENT
2025-11-03 21:38:17.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect-Self-Updater:  Checking https://saastest.app.blackduck.com/api/tools/detect API for centrally managed Detect version to download to /Users/madhusud/tmp.
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] WARNING: --- Detect-Self-Updater:  Unable to download jar from https://saastest.app.blackduck.com/api/tools/detect.
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] WARNING: --- Detect-Self-Updater:  Response code from https://saastest.app.blackduck.com/api/tools/detect was: 400 Bad Request
2025-11-03 21:38:20.7514 IST [Blackduck SCA Detect Execution] INFO: ______     _            _
2025-11-03 21:38:20.7515 IST [Blackduck SCA Detect Execution] INFO: |  _  \   | |          | |
2025-11-03 21:38:20.7515 IST [Blackduck SCA Detect Execution] INFO: | | | |___| |_ ___  ___| |_
2025-11-03 21:38:20.7515 IST [Blackduck SCA Detect Execution] INFO: | | | / _ \ __/ _ \/ __| __|
2025-11-03 21:38:20.7515 IST [Blackduck SCA Detect Execution] INFO: | |/ /  __/ ||  __/ (__| |_
2025-11-03 21:38:20.7515 IST [Blackduck SCA Detect Execution] INFO: |___/ \___|\__\___|\___|\__|
2025-11-03 21:38:20.7515 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-03 21:38:20.8426 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-03 21:38:20.8426 IST [Blackduck SCA Detect Execution] INFO: Detect Version: 11.0.0
2025-11-03 21:38:20.8426 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Current property values:
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- --property = value [notes]
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ------------------------------------------------------------
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.api.token = **************************************************************************************************** [cmd] 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.offline.mode = false [cmd] 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.url = https://saastest.app.blackduck.com [cmd] 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.bdio.file.name = scan [cmd] 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.bdio.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact [cmd] 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.blackduck.scan.mode = INTELLIGENT [cmd] 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.cleanup = false [cmd] 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.diagnostic = true [cmd] 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.excluded.directories = /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge [env] 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect [cmd] 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.project.name = MBP_Github_BlackduckSca_Test [env] 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.wait.for.results = true [cmd] 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ------------------------------------------------------------
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:38:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect build date: 2025-10-30
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Source directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Output directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Run directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834
2025-11-03 21:38:21.0349 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-03 21:38:21.0349 IST [Blackduck SCA Detect Execution] INFO: ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
2025-11-03 21:38:21.0349 IST [Blackduck SCA Detect Execution] INFO: Diagnostic mode on.
2025-11-03 21:38:21.0349 IST [Blackduck SCA Detect Execution] INFO: A zip file will be created with logs and relevant Detect output files.
2025-11-03 21:38:21.0350 IST [Blackduck SCA Detect Execution] INFO: It is generally not recommended to leave diagnostic mode on as you must manually clean up the zip.
2025-11-03 21:38:21.0350 IST [Blackduck SCA Detect Execution] INFO: ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
2025-11-03 21:38:21.0350 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Initializing diagnostic components.
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/reports/search_report.txt
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/reports/search_detailed_report.txt
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/reports/detector_report.txt
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/reports/detector_profile_report.txt
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/reports/code_location_report.txt
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/reports/dependency_counts_report.txt
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/reports/detect_configuration.txt
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Attempting to capture sysout.
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Writing sysout to file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/logs/sysout.txt
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Attempting to set 'com.blackduck.integration' logging level.
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Attempting to capture additional log messages to files.
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Redirected to file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/logs/all.txt
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Redirected to file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/logs/debug.txt
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Redirected to file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/logs/info.txt
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Attempting to restrict console to debug level (additional levels written to files).
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Adding additional log listeners to extractions.
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Diagnostics is now in control of logging!
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Creating configuration diagnostics reports.
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Diagnostics system is ready.
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Main boot completed. Deciding what Detect should do.
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Black Duck SCA will run ONLINE: A Black Duck SCA url was found.
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Decided what products will be run. Starting product boot.
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect product boot start.
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Will boot Black Duck SCA product.
2025-11-03 21:38:21.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect will check communication with the Black Duck SCA server.
2025-11-03 21:38:28.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Successfully connected to Black Duck SCA (version 2025.7.1)!
2025-11-03 21:38:28.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Connected as: sa_centralintegrations
2025-11-03 21:38:28.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Server Roles: Global Project Administrator, Global Notification Viewer, Global Release Creator, Global Security Manager, Global Code Scanner, Project Creator, Global Project Viewer, Integration Manager, Global Project Manager, Custom Fields Administrator, Lite Global Project Manager, Policy Manager, License Manager, Component Manager, Copyright Editor
2025-11-03 21:38:29.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Groups: 
2025-11-03 21:38:30.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- You seem to be running in a MAC operating system.
2025-11-03 21:38:30.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- You seem to be using aarch64 architecture.
2025-11-03 21:38:30.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Downloading phone home credentials.
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect product boot completed.
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect boot completed.
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect will attempt to run.
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Guessed Detect jar location as /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0/detect-11.0.0.jar
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Checking for jar file: /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0/detect-11.0.0.jar
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Found detect jar file.
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Docker tool.
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Was not applicable.
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Docker actions finished.
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Bazel tool.
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Was not applicable.
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Bazel actions finished.
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:38:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Detectors tool.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Starting detector file system traversal.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Searching for detectors.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- filteredSubDirectories: [/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/Gruntfile.js, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/CODE_OF_CONDUCT.md, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/artifacts, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/nodemon.json, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/cypress.json, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/app, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/LICENSE, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/test, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/app.json, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/config, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/server.js, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/Dockerfile, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/README.md, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package-lock.json, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package.json, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/CONTRIBUTING.md, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/Jenkinsfile, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/docker-compose.yml, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/Procfile]
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Evaluating detectors. This may take a while.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Determining applicable detectors on the directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Attempting NpmPackageLockDetectable
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Processing project.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Found 658 packages in the lockfile.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Found 36 root dependencies.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detector Type NPM Entry Point NPM Package Lock applied and was attempted
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detector results ("true" = succeeded): [NPM Package Lock: true]
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Found (1) applicable detectors in: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Finished detectors.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======================================================================================================
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detector Report
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======================================================================================================
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 	/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm (depth 0)
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 		NPM Package Lock: SUCCESS
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package-lock.json
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package.json
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Publishing file events.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Saved file to diagnostics zip: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package-lock.json
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Saved file to diagnostics zip: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package.json
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- A valid preferred detector type was not provided, deciding project name automatically.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Exactly one unique detector was found. Using NPM found at depth 0 as project info.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Finished evaluating detectors for project info.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Finished running detectors.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- ======================================================================================================
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Search results
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- ======================================================================================================
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 	FOUND: NPM
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- ======================================================================================================
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detectors actions finished.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Completed code location tools.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Determining project info.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Using the first ordered tool with project info: DETECTOR
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Project name: MBP_Github_BlackduckSca_Test
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Project version: 1.3.0
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Integrated Matching Correlation ID: 039991a0-1415-4267-9aaa-c18febe2848e
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- BDIO Generated: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact/scan.bdio
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- No clone project or version name supplied. Will not clone.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- No project group was supplied. Will not assign a project group.
2025-11-03 21:38:32.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- No project version licenses were supplied.  Will not update licenses.
2025-11-03 21:38:34.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- No 'Application ID' to set.
2025-11-03 21:38:34.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- No custom fields to set.
2025-11-03 21:38:34.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Completed project and version actions.
2025-11-03 21:38:34.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Processing Detect Code Locations.
2025-11-03 21:38:36.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Scan initiated with scan service. Scan ID received: cf8cc6f2-3545-4773-9603-54f3f0df8926
2025-11-03 21:38:36.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Successfully completed package manager scan of file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact/scan.bdio
2025-11-03 21:38:36.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Uploading scan.bdio
2025-11-03 21:38:38.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Starting the codelocation file uploads.
2025-11-03 21:38:38.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] DEBUG: --- Uploading BDIO file /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact/scan.bdio
2025-11-03 21:38:38.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] DEBUG: --- BDIO upload file count = 1
2025-11-03 21:38:38.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] DEBUG: --- Starting upload to https://saastest.app.blackduck.com/api/intelligent-persistence-scans/cf8cc6f2-3545-4773-9603-54f3f0df8926
2025-11-03 21:38:38.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] DEBUG: --- Appending file bdio-entry-00.jsonld, to https://saastest.app.blackduck.com/api/intelligent-persistence-scans/cf8cc6f2-3545-4773-9603-54f3f0df8926 with count 1
2025-11-03 21:38:42.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] DEBUG: --- Finishing upload to https://saastest.app.blackduck.com/api/intelligent-persistence-scans/cf8cc6f2-3545-4773-9603-54f3f0df8926 with count 1
2025-11-03 21:38:43.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] INFO: --- Try #1 for task bdio upload (elapsed: 00:00:00.000)...complete!
2025-11-03 21:38:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Completed the codelocation file uploads.
2025-11-03 21:38:43.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Completed Detect Code Location processing.
2025-11-03 21:38:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:38:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Signature Scanner tool.
2025-11-03 21:38:43.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Signature scanner will use the Black Duck SCA server to download/update the scanner - this is the most likely situation.
2025-11-03 21:38:43.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Using Tools Scan CLI download API (new).
2025-11-03 21:38:43.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- The directory structure was likely created by the installer
2025-11-03 21:38:43.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Locally installed signature scanner version: 1.0.6
2025-11-03 21:38:47.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Locally installed Signature Scanner version is up to date - skipping download.
2025-11-03 21:38:47.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- The directory structure was likely created by the installer
2025-11-03 21:38:47.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- The Black Duck Signature Scanner downloaded/found successfully: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools
2025-11-03 21:38:47.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- No scan targets provided - registering the source path /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm to scan
2025-11-03 21:38:49.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Starting the Black Duck Signature Scan commands.
2025-11-03 21:38:49.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] DEBUG: --- The directory structure was likely created by the installer
2025-11-03 21:38:49.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] DEBUG: --- Using this java installation : /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/jre/Contents/Home/bin/java
2025-11-03 21:38:49.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] DEBUG: --- Using the Black Duck hostname : 'saastest.app.blackduck.com'
2025-11-03 21:38:49.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- Black Duck CLI command: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/jre/Contents/Home/bin/java -Done-jar.silent=true -Done-jar.jar.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/lib/cache/scan.cli.impl-standalone.jar -Xmx4096m -jar /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/lib/scan.cli-1.0.6-standalone.jar --no-prompt --scheme https --host saastest.app.blackduck.com --port 443 -v --logDir /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1 --statusWriteDir /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1 --project MBP_Github_BlackduckSca_Test --release 1.3.0 --name nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature --exclude /node_modules/ --exclude /.bridge/ --scass-scan /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
2025-11-03 21:38:51.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Start wrapper: ScanCliWrapperSettings [commandLine=[args=[Ljava.lang.String;@3148f668, options=[Lorg.apache.commons.cli.Option;@6e005dc9], fileUriSet=null, scheme=https, host=saastest.app.blackduck.com, port=443]...
2025-11-03 21:38:52.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Start scan loop: ScanClientSettings [commandLine=[--no-prompt, --scheme, https, --host, saastest.app.blackduck.com, --port, 443, -v, --logDir, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1, --statusWriteDir, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1, --project, MBP_Github_BlackduckSca_Test, --release, 1.3.0, --name, nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature, --exclude, /node_modules/, --exclude, /.bridge/, --scass-scan, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm], fileUriSet=[file://BD-MB83224/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm], uploadCSV=false, dryRunWriteDir=No dry run file., outputFormat=null, scanId=null, dryRunReadFile=No dry run file., fsScanReadyWaitingPeriod=30, snippetMatching=false, snippetMatchingOnly=false, snippetMatchingAllSource=false, fullSnippetScan=false, uploadSource=false, individualFileMatching=none, licenseSearch=false, copyrightSearch=false, signatureGeneration=false, noSignatureGeneration=false, maxRequestBodySize=20000000, maxUpdateSize=10000, matchConfidenceThreshold=null, minScanInterval=null, logDir=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1, scheme=https, host=saastest.app.blackduck.com, port=443, name=Optional[nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature], project=Optional[MBP_Github_BlackduckSca_Test], release=Optional[1.3.0], username=null, password=<NOT SHOWN>, correlationId=null, noPersistence=false, noPersistenceMode=null, retainUnmatchedFiles=null, projectGroupName=null, scassScan=true]...
2025-11-03 21:38:52.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Individual File Matching Detected: none...
2025-11-03 21:38:52.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Finalized sha1 white list: []...
2025-11-03 21:38:52.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Finalized clean sha1 white list: []...
2025-11-03 21:38:52.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Initialize client for saastest.app.blackduck.com:443
2025-11-03 21:38:54.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Scan engine initialized with niceness set to false
2025-11-03 21:38:55.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Dry Run path: Optional.empty
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: ScanExecResult: ScanExecResult [scanClientSettings=ScanClientSettings [commandLine=[--no-prompt, --scheme, https, --host, saastest.app.blackduck.com, --port, 443, -v, --logDir, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1, --statusWriteDir, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1, --project, MBP_Github_BlackduckSca_Test, --release, 1.3.0, --name, nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature, --exclude, /node_modules/, --exclude, /.bridge/, --scass-scan, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm], fileUriSet=[file://BD-MB83224/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm], uploadCSV=false, dryRunWriteDir=No dry run file., outputFormat=null, scanId=null, dryRunReadFile=No dry run file., fsScanReadyWaitingPeriod=30, snippetMatching=false, snippetMatchingOnly=false, snippetMatchingAllSource=false, fullSnippetScan=false, uploadSource=false, individualFileMatching=none, licenseSearch=false, copyrightSearch=false, signatureGeneration=false, noSignatureGeneration=false, maxRequestBodySize=20000000, maxUpdateSize=10000, matchConfidenceThreshold=null, minScanInterval=null, logDir=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1, scheme=https, host=saastest.app.blackduck.com, port=443, name=Optional[nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature], project=Optional[MBP_Github_BlackduckSca_Test], release=Optional[1.3.0], username=null, password=<NOT SHOWN>, correlationId=null, noPersistence=false, noPersistenceMode=null, retainUnmatchedFiles=null, projectGroupName=null, scassScan=true], result=0, dataFileName=2025_11_03_21_38_5418369868617608293306.tmp, scanContainer=null, sigGenScanContainer=SigGenScanContainerView{baseDir=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm, hostName=BD-MB83224, name=nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature, scannerVersion=1.0.6, signatureVersion=7.0.0, ownerEntityKeyToken=SN#BD-MB83224-nodejs-npm, createdOn=2025-11-03T16:08:54.757Z, timeToScan=152, scanNodeList.size()=30, scanLeafList.size()=105, scanProblem=null, scanProblemList.size()=0}, fpScanContainer=null, stringSearchScanContainer=null, scanResult=ScanView{id=fb67e2fe-e991-4dee-8a49-18de60cbe0f4, scannerVersion=1.0.6, signatureVersion=7.0.0, name=nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature, hostName=BD-MB83224, ownerEntityKeyToken=SN#BD-MB83224-nodejs-npm, baseDir=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm, createdOn=2025-11-03T16:08:54.757Z, matchCount=0, numDirs=0, numNonDirFiles=0, statusMessage=file://BD-MB83224/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm, deepSystemSize=Optional.empty, timeLastModified=0, timeToPersistMs=0, scanTime=0, arguments={}, debugMode=false}, scanSummary=ScanSummaryView{scanState=STARTED, transitionReason=SCAN_INGESTED, statusMessage=, createdAt=2025-11-03T16:08:54.989Z, updatedAt=2025-11-03T16:08:59.523Z, createdByUserName=Optional[sa_centralintegrations], scanSize=Optional[2972034], serverVersion=2025.7.1, matchCount=0, directoryCount=Optional[0], fileCount=Optional[0], baseDirectory=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm, hostName=BD-MB83224, scanType=SIGNATURE, errorCode=Optional.empty, retainUnmatchedFiles=false, resourceMetadata=MetaDataView{href=https://saastest.app.blackduck.com/api/scan-summaries/fb67e2fe-e991-4dee-8a49-18de60cbe0f4, links=[LinkView{rel=codelocation, href=https://saastest.app.blackduck.com/api/codelocations/0f1467b4-867f-498d-9341-a2c5738b6056}]}}, scanDate=Mon Nov 03 21:38:52 IST 2025, scanEndDate=Mon Nov 03 21:39:00 IST 2025, scanCreated=false, uploadUrl=null, uploadUrlData=null]
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Creating data output file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1/log/BD-MB83224-nodejs-npm-2025-11-03T160854.757Z.log
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Logging to file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1/log/BD-MB83224-nodejs-npm-2025-11-03T160854.757Z.log
2025-11-03 21:39:00.4667 IST [Blackduck SCA Detect Execution] INFO: Logging to file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1/log/BD-MB83224-nodejs-npm-2025-11-03T160854.757Z.log
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Persist scan output to file...
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Persisted status: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1/output/scanOutput.json
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Creating data output file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1/status/BD-MB83224-nodejs-npm-2025-11-03T160854.757Z.json
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Persist ScanSummary to file...
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] DEBUG: --- INFO: Persisted status: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1/status/BD-MB83224-nodejs-npm-2025-11-03T160854.757Z.json
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- 
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- Black Duck Signature Scanner return code: 0
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- Signature Scanner log output directory: '/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1'
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Completed the Black Duck Signature Scan commands.
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Signature Scanner actions finished.
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Binary Scanner tool.
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Invoking intelligent persistent binary scan.
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Binary scanner found nothing to upload.
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Binary Scanner actions finished.
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Container Scanner tool.
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Invoking intelligent persistent container scan.
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Determining if configuration is valid to run a container scan.
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- No detect.container.scan.file.path property was provided. Skipping container scan.
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Container Scanner actions finished.
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Vulnerability Impact Analysis tool will not be run.
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- IaC Scanner tool will not be run.
2025-11-03 21:39:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:39:01.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #1 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/fb67e2fe-e991-4dee-8a49-18de60cbe0f4 (elapsed: 00:00:00.000)...not done yet, waiting 1 seconds and trying again...
2025-11-03 21:39:03.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #2 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/fb67e2fe-e991-4dee-8a49-18de60cbe0f4 (elapsed: 00:00:01.950)...not done yet, waiting 2 seconds and trying again...
2025-11-03 21:39:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #3 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/fb67e2fe-e991-4dee-8a49-18de60cbe0f4 (elapsed: 00:00:04.863)...not done yet, waiting 3 seconds and trying again...
2025-11-03 21:39:10.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #4 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/fb67e2fe-e991-4dee-8a49-18de60cbe0f4 (elapsed: 00:00:08.944)...complete!
2025-11-03 21:39:11.0000 IST [Blackduck SCA Detect Execution][main] WARNING: --- Encountered unexpected scan status: NOT_INCLUDED
2025-11-03 21:39:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #1 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/cf8cc6f2-3545-4773-9603-54f3f0df8926 (elapsed: 00:00:00.000)...complete!
2025-11-03 21:39:11.0000 IST [Blackduck SCA Detect Execution][main] ERROR: --- BOM Scan Status: NOT_INCLUDED - Black Duck SCA failed to prepare BOM for the scan.
2025-11-03 21:39:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Checking to see if Detect should check policy for violations.
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][pool-2-thread-1] DEBUG: --- Starting phone home
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][pool-2-thread-1] DEBUG: --- Phoning home to https://www.google-analytics.com/mp/collect?api_secret=LA7cz8EKSLCmHdHdVdThGA&measurement_id=G-J4L8680QKM
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Creating status file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-08-20-834/status/status.json
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect shutdown begin.
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Finishing diagnostic mode.
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Finishing reports.
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Finishing logging.
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Finishing executable capture.
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Finishing file capture.
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Creating diagnostics zip.
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Diagnostics zip location: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/detect-run-2025-11-03-16-08-20-834.zip
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: status/status.json
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1/output/scanOutput.json
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1/status/BD-MB83224-nodejs-npm-2025-11-03T160854.757Z.json
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1/CLI_Output.txt
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: scan/BlackDuckScanOutput/2025-11-03_16-08-49-866_1/log/BD-MB83224-nodejs-npm-2025-11-03T160854.757Z.log
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: scan/.bdignore
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: logs/all.txt
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: logs/debug.txt
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: logs/info.txt
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: logs/sysout.txt
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: relevant/FILE-1-package.json
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: relevant/FILE-MAP.txt
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: relevant/FILE-0-package-lock.json
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/search_report.txt
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/detector_report.txt
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/dependency_counts_report.txt
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/search_detailed_report.txt
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/detect_configuration.txt
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/code_location_report.txt
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/detector_profile_report.txt
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Diagnostics file created at: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/detect-run-2025-11-03-16-08-20-834.zip
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Diagnostic mode has completed.
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Skipping cleanup, it is disabled.
2025-11-03 21:39:12.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Ending phone home.
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][pool-2-thread-1] DEBUG: --- Completed phone home
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect shutdown completed.
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- All Detect actions completed.
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- === Additional  Information ===
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- ====== Detect Operations ======
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Execute Detectors: SUCCESS
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- SubProject Aggregate: SUCCESS
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Package_manager Upload: SUCCESS
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Upload Intelligent Persistent Bdio: SUCCESS
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Create Online Signature Scan Batch: SUCCESS
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Execute Signature Scan CLI: SUCCESS
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Retrieve Container Scan Image File: SUCCESS
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- ===============================
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======== Detect Result ========
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Black Duck SCA Project BOM: https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/components
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======== Detect Status ========
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- NPM: SUCCESS
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Signature scan / Snippet scan on /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm: SUCCESS
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] ERROR: --- Overall Status: FAILURE_BOM_PREPARATION - Black Duck SCA failed to prepare BOM for the scan.
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- If you need help troubleshooting this problem, generate a diagnostic zip file by adding '-d' to the command line, and provide it to Black Duck Technical Support. See 'Diagnostic Mode' in the Detect documentation for more information.
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ===============================
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect duration: 00h 00m 56s 554ms
2025-11-03 21:39:13.0000 IST [Blackduck SCA Detect Execution][main] ERROR: --- Exiting with code 30 - FAILURE_BOM_PREPARATION
2025-11-03 21:39:13.5041 IST [Blackduck SCA Detect Execution] ERROR: exit status 30
2025-11-03 21:39:13.5160 IST [Blackduck SCA Detect Execution] INFO: Provided value for resource 'detect.results.path'
2025-11-03 21:39:13.5160 IST [Blackduck SCA Detect Execution] DEBUG: Provided value '/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect' for resource 'detect.results.path'
2025-11-03 21:39:13.5164 IST [Blackduck SCA Detect Execution] ERROR: Adapter failed: exit status 1
2025-11-03 21:39:13.5665 IST [Blackduck SCA Results] INFO: Skipping Blackduck SCA issues retrieval as "blackducksca.fixpr.enabled" is configured to false
2025-11-03 21:39:13.5727 IST [Blackduck SCA Results] INFO: Adapter finished
2025-11-03 21:39:13.6207 IST [SCM Checker] DEBUG: JENKINS_HOME is set to value: "/Users/madhusud/.jenkins"
2025-11-03 21:39:13.6260 IST [SCM Checker] INFO: Provided value for resource 'jenkins.enabled'
2025-11-03 21:39:13.6260 IST [SCM Checker] DEBUG: Provided value 'true' for resource 'jenkins.enabled'
2025-11-03 21:39:13.6261 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-policy-violations-fetcher
2025-11-03 21:39:13.6265 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Policy Violations Fetcher
2025-11-03 21:39:13.6267 IST [SCM Checker] INFO: Adapter finished
2025-11-03 21:39:13.6579 IST [Detect Component Locator] INFO: skipping fix pull requests creation as "blackducksca.fixpr.enabled" is configured to false
2025-11-03 21:39:13.6634 IST [Detect Component Locator] INFO: Adapter finished
2025-11-03 21:39:13.6963 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Jenkins is enabled
2025-11-03 21:39:13.6967 IST [Blackduck SCA Policy Violations Fetcher] ERROR: There is no detect scan to gather results from
2025-11-03 21:39:13.7021 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.projectBomUrl'
2025-11-03 21:39:13.7021 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Provided value '' for resource 'blackducksca.projectBomUrl'
2025-11-03 21:39:13.7023 IST [Blackduck SCA Policy Violations Fetcher] INFO: Adapter finished
******************************* END EXECUTION OF BRIDGE CLI *******************************
[Security Scan] INFO: Archiving DIAGNOSTIC jenkins artifact from: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge
Archiving artifacts
[Security Scan] INFO: DIAGNOSTIC archived successfully in jenkins artifact
[Security Scan] INFO: Retrieving the issue count from the scan results
[Security Scan] INFO: Issue count not found in output file
[Security Scan] ERROR: Workflow failed! Exit code 2: Error from adapter
[Security Scan] INFO: Marking build status as FAILURE is ignored since exit code is: 2
**************************** END EXECUTION OF BLACK DUCK SECURITY SCAN ****************************
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // dir
[Pipeline] }
[Pipeline] // script
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Declarative: Post Actions)
[Pipeline] echo
Black Duck Logs Publisher - Starting log upload process
[Pipeline] echo
Configuration: [githubOrg:blackducksca-jenkins-samples, repoName:full-scan, credentialsId:github-pat-logs-publisher, maxRetries:3, retentionCount:10, jobNamePrefixes:[MBP_Github_, MBP_, Github_, Pipeline_, Job_, Build_]]
[Pipeline] echo
Job Name: MBP_Github_BlackduckSca_Test/main
[Pipeline] echo
Build Number: 44
[Pipeline] echo
GitHub Organization: blackducksca-jenkins-samples
[Pipeline] withCredentials
Masking supported pattern matches of $GITHUB_TOKEN
[Pipeline] {
[Pipeline] echo
Using configured repository name: full-scan
[Pipeline] echo
Target repository: blackducksca-jenkins-samples/full-scan
[Pipeline] echo
LogProcessor: captureJenkinsLogs called
```

---

*Log generated by Black Duck Logs Publisher*