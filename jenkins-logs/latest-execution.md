# Jenkins Execution Log

## Build Information
- **Job Name:** `MBP_Github_BlackduckSca_Test/main`
- **Build Number:** #40
- **Build Status:** 🟢 **SUCCESS**
- **Duration:** 4 min 25 sec and counting
- **Timestamp:** 2025-11-03 19:38:36 UTC
- **Build URL:** http://localhost:8080/job/MBP_Github_BlackduckSca_Test/job/main/40/

---

## Console Output

```
Started by user admin
Connecting to https://api.github.com using madhusud@blackduck.com/****** (Github_Username_PAT)
Obtained nodejs-npm/Jenkinsfile from 210500bef137b1eb0f6b5587d60f61555fd7c67f
Loading library blackduck-logs-publisher@main
Attempting to resolve main from remote references...
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git ls-remote -h -- https://github.com/integrations-garage/blackduck-logs-publisher # timeout=10
Found match: refs/heads/main revision 9f7bac4b45809e3114c1d802d79a99b0287c5131
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
Checking out Revision 9f7bac4b45809e3114c1d802d79a99b0287c5131 (main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 9f7bac4b45809e3114c1d802d79a99b0287c5131 # timeout=10
Commit message: "Phase 1A"
 > git rev-list --no-walk 9f7bac4b45809e3114c1d802d79a99b0287c5131 # timeout=10
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
Checking out Revision 210500bef137b1eb0f6b5587d60f61555fd7c67f (main)
Commit message: "Black Duck SCA Build Scan"
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 210500bef137b1eb0f6b5587d60f61555fd7c67f # timeout=10
 > git rev-list --no-walk 3c8a18cce43eeaa714e95defaa0b808f02310fb1 # timeout=10
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
[Security Scan] INFO: Executable command line arguments: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm/bridge-cli --stage blackducksca --input /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/blackducksca_input15318053636608931580.json --out .bridge/output/scan_info_out.json --diagnostics

******************************* START EXECUTION OF BRIDGE CLI *******************************
2025-11-03 19:37:24.9385 IST [Bridge CLI] INFO: Using cache directory: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
2025-11-03 19:37:24.9508 IST [Bridge CLI] INFO: Found version "3.0.143" in registry for workflow "blackducksca", trying to load it from local cache
2025-11-03 19:37:24.9572 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA Controller
2025-11-03 19:37:24.9576 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA Results
2025-11-03 19:37:24.9577 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA Detect Execution
2025-11-03 19:37:24.9580 IST [Bridge CLI] DEBUG: New adapter loaded: Detect Component Locator
2025-11-03 19:37:24.9583 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA SARIF Issues Fetcher
2025-11-03 19:37:24.9586 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA SARIF Generator
2025-11-03 19:37:24.9589 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA Gitlab Reports Generator
2025-11-03 19:37:24.9591 IST [Bridge CLI] DEBUG: New adapter loaded: Blackduck SCA Policy Violations Fetcher
2025-11-03 19:37:24.9730 IST [Bridge CLI] DEBUG: New adapter loaded: Downloader Adapter
2025-11-03 19:37:24.9911 IST [Bridge CLI] DEBUG: New adapter loaded: SCM Checker
2025-11-03 19:37:24.9927 IST [Bridge CLI] DEBUG: New adapter loaded: GitHub Badges
2025-11-03 19:37:25.0014 IST [Bridge CLI] DEBUG: New adapter loaded: GitHub Pull Request Handler
2025-11-03 19:37:25.0015 IST [Bridge CLI] DEBUG: New adapter loaded: GitLab Pull Request Handler
2025-11-03 19:37:25.0016 IST [Bridge CLI] DEBUG: New adapter loaded: Azure Pull Request Handler
2025-11-03 19:37:25.0018 IST [Bridge CLI] DEBUG: New adapter loaded: Bitbucket Pull Request Handler
2025-11-03 19:37:25.0146 IST [Bridge CLI] DEBUG: New adapter loaded: GitHub Commenter
2025-11-03 19:37:25.0147 IST [Bridge CLI] DEBUG: New adapter loaded: Gitlab Commenter
2025-11-03 19:37:25.0148 IST [Bridge CLI] DEBUG: New adapter loaded: Azure Commenter
2025-11-03 19:37:25.0148 IST [Bridge CLI] DEBUG: New adapter loaded: Bitbucket Commenter
2025-11-03 19:37:25.0348 IST [Bridge CLI] DEBUG: New adapter loaded: Detect Installer
2025-11-03 19:37:25.0730 IST [Bridge CLI] INFO: Input Resources:
2025-11-03 19:37:25.0730 IST [Bridge CLI] INFO: resource = value [source]
2025-11-03 19:37:25.0730 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-03 19:37:25.0730 IST [Bridge CLI] INFO: blackducksca.scan.full = true [blackducksca_input15318053636608931580.json]
2025-11-03 19:37:25.0730 IST [Bridge CLI] INFO: blackducksca.token = ***************************************** [blackducksca_input15318053636608931580.json]
2025-11-03 19:37:25.0730 IST [Bridge CLI] INFO: blackducksca.url = https://saastest.app.blackduck.com [blackducksca_input15318053636608931580.json]
2025-11-03 19:37:25.0730 IST [Bridge CLI] INFO: blackducksca.waitForScan = true [blackducksca_input15318053636608931580.json]
2025-11-03 19:37:25.0731 IST [Bridge CLI] INFO: network.airgap = false [blackducksca_input15318053636608931580.json]
2025-11-03 19:37:25.0731 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-03 19:37:25.0731 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca
2025-11-03 19:37:25.0734 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Controller
2025-11-03 19:37:25.0810 IST [Bridge CLI] DEBUG: New adapter loaded: Check pull request
2025-11-03 19:37:25.0811 IST [Bridge CLI] INFO: Starting Adapter: Check pull request
2025-11-03 19:37:25.1094 IST [Check pull request] INFO: Provided value for resource 'environment.scan.pull'
2025-11-03 19:37:25.1094 IST [Check pull request] DEBUG: Provided value 'false' for resource 'environment.scan.pull'
2025-11-03 19:37:25.1096 IST [Check pull request] INFO: Adapter finished
2025-11-03 19:37:26.1296 IST [Blackduck SCA Controller] INFO: Found Black Duck SCA Detect jar file "detect-11.0.0.jar" in "/Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0"
2025-11-03 19:37:26.1516 IST [Blackduck SCA Controller] INFO: Provided value for resource 'detect.execution.path'
2025-11-03 19:37:26.1517 IST [Blackduck SCA Controller] DEBUG: Provided value '/Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0/detect-11.0.0.jar' for resource 'detect.execution.path'
2025-11-03 19:37:26.1518 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-detect
2025-11-03 19:37:26.1518 IST [Bridge CLI] INFO: Starting adapters for stage scm
2025-11-03 19:37:26.1518 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-post-processing
2025-11-03 19:37:26.1540 IST [Bridge CLI] INFO: Starting Adapter: SCM Checker
2025-11-03 19:37:26.1540 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Results
2025-11-03 19:37:26.1540 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Detect Execution
2025-11-03 19:37:26.1553 IST [Blackduck SCA Controller] INFO: Adapter finished
2025-11-03 19:37:26.1540 IST [Bridge CLI] INFO: Starting Adapter: Detect Component Locator
2025-11-03 19:37:26.2386 IST [Blackduck SCA Detect Execution] INFO: Running command /Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home/bin/java -jar /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0/detect-11.0.0.jar --detect.cleanup=false --detect.bdio.file.name=scan --detect.bdio.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact --detect.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect --detect.diagnostic=true --blackduck.offline.mode=false --blackduck.url=https://saastest.app.blackduck.com --blackduck.api.token= --detect.wait.for.results=true --detect.blackduck.scan.mode=INTELLIGENT
2025-11-03 19:37:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect-Self-Updater:  Checking https://saastest.app.blackduck.com/api/tools/detect API for centrally managed Detect version to download to /Users/madhusud/tmp.
2025-11-03 19:37:30.0000 IST [Blackduck SCA Detect Execution][main] WARNING: --- Detect-Self-Updater:  Unable to download jar from https://saastest.app.blackduck.com/api/tools/detect.
2025-11-03 19:37:30.0000 IST [Blackduck SCA Detect Execution][main] WARNING: --- Detect-Self-Updater:  Response code from https://saastest.app.blackduck.com/api/tools/detect was: 400 Bad Request
2025-11-03 19:37:31.2125 IST [Blackduck SCA Detect Execution] INFO: ______     _            _
2025-11-03 19:37:31.2126 IST [Blackduck SCA Detect Execution] INFO: |  _  \   | |          | |
2025-11-03 19:37:31.2126 IST [Blackduck SCA Detect Execution] INFO: | | | |___| |_ ___  ___| |_
2025-11-03 19:37:31.2126 IST [Blackduck SCA Detect Execution] INFO: | | | / _ \ __/ _ \/ __| __|
2025-11-03 19:37:31.2127 IST [Blackduck SCA Detect Execution] INFO: | |/ /  __/ ||  __/ (__| |_
2025-11-03 19:37:31.2127 IST [Blackduck SCA Detect Execution] INFO: |___/ \___|\__\___|\___|\__|
2025-11-03 19:37:31.2127 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-03 19:37:31.3117 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-03 19:37:31.3117 IST [Blackduck SCA Detect Execution] INFO: Detect Version: 11.0.0
2025-11-03 19:37:31.3117 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Current property values:
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- --property = value [notes]
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ------------------------------------------------------------
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.api.token = **************************************************************************************************** [cmd] 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.offline.mode = false [cmd] 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.url = https://saastest.app.blackduck.com [cmd] 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.bdio.file.name = scan [cmd] 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.bdio.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact [cmd] 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.blackduck.scan.mode = INTELLIGENT [cmd] 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.cleanup = false [cmd] 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.diagnostic = true [cmd] 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.excluded.directories = /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge [env] 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect [cmd] 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.project.name = MBP_Github_BlackduckSca_Test [env] 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.wait.for.results = true [cmd] 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ------------------------------------------------------------
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect build date: 2025-10-30
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Source directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Output directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Run directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303
2025-11-03 19:37:31.4665 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-03 19:37:31.4665 IST [Blackduck SCA Detect Execution] INFO: ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
2025-11-03 19:37:31.4665 IST [Blackduck SCA Detect Execution] INFO: Diagnostic mode on.
2025-11-03 19:37:31.4665 IST [Blackduck SCA Detect Execution] INFO: A zip file will be created with logs and relevant Detect output files.
2025-11-03 19:37:31.4665 IST [Blackduck SCA Detect Execution] INFO: It is generally not recommended to leave diagnostic mode on as you must manually clean up the zip.
2025-11-03 19:37:31.4666 IST [Blackduck SCA Detect Execution] INFO: ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
2025-11-03 19:37:31.4666 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Initializing diagnostic components.
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/reports/search_report.txt
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/reports/search_detailed_report.txt
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/reports/detector_report.txt
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/reports/detector_profile_report.txt
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/reports/code_location_report.txt
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/reports/dependency_counts_report.txt
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Created report file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/reports/detect_configuration.txt
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Attempting to capture sysout.
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Writing sysout to file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/logs/sysout.txt
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Attempting to set 'com.blackduck.integration' logging level.
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Attempting to capture additional log messages to files.
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Redirected to file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/logs/all.txt
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Redirected to file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/logs/debug.txt
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Redirected to file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/logs/info.txt
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Attempting to restrict console to debug level (additional levels written to files).
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Adding additional log listeners to extractions.
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Diagnostics is now in control of logging!
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Creating configuration diagnostics reports.
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Diagnostics system is ready.
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Main boot completed. Deciding what Detect should do.
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Black Duck SCA will run ONLINE: A Black Duck SCA url was found.
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Decided what products will be run. Starting product boot.
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect product boot start.
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Will boot Black Duck SCA product.
2025-11-03 19:37:31.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect will check communication with the Black Duck SCA server.
2025-11-03 19:37:39.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Successfully connected to Black Duck SCA (version 2025.7.1)!
2025-11-03 19:37:39.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Connected as: sa_centralintegrations
2025-11-03 19:37:39.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Server Roles: Global Project Administrator, Global Notification Viewer, Global Release Creator, Global Security Manager, Global Code Scanner, Project Creator, Global Project Viewer, Integration Manager, Global Project Manager, Custom Fields Administrator, Lite Global Project Manager, Policy Manager, License Manager, Component Manager, Copyright Editor
2025-11-03 19:37:39.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Groups: 
2025-11-03 19:37:41.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- You seem to be running in a MAC operating system.
2025-11-03 19:37:41.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- You seem to be using aarch64 architecture.
2025-11-03 19:37:41.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Downloading phone home credentials.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect product boot completed.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect boot completed.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect will attempt to run.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Guessed Detect jar location as /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0/detect-11.0.0.jar
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Checking for jar file: /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0/detect-11.0.0.jar
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Found detect jar file.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Docker tool.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Was not applicable.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Docker actions finished.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Bazel tool.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Was not applicable.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Bazel actions finished.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Detectors tool.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Starting detector file system traversal.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Searching for detectors.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- filteredSubDirectories: [/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/Gruntfile.js, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/CODE_OF_CONDUCT.md, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/artifacts, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/nodemon.json, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/cypress.json, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/app, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/LICENSE, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/test, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/app.json, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/config, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/server.js, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/Dockerfile, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/README.md, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package-lock.json, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package.json, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/CONTRIBUTING.md, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/Jenkinsfile, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/docker-compose.yml, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/Procfile]
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Evaluating detectors. This may take a while.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Determining applicable detectors on the directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Attempting NpmPackageLockDetectable
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Processing project.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Found 658 packages in the lockfile.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Found 36 root dependencies.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detector Type NPM Entry Point NPM Package Lock applied and was attempted
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detector results ("true" = succeeded): [NPM Package Lock: true]
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Found (1) applicable detectors in: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Finished detectors.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======================================================================================================
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detector Report
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======================================================================================================
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 	/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm (depth 0)
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 		NPM Package Lock: SUCCESS
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package-lock.json
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package.json
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Publishing file events.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Saved file to diagnostics zip: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package-lock.json
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Saved file to diagnostics zip: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package.json
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- A valid preferred detector type was not provided, deciding project name automatically.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Exactly one unique detector was found. Using NPM found at depth 0 as project info.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Finished evaluating detectors for project info.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Finished running detectors.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- ======================================================================================================
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Search results
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- ======================================================================================================
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 	FOUND: NPM
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- ======================================================================================================
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detectors actions finished.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Completed code location tools.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Determining project info.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Using the first ordered tool with project info: DETECTOR
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Project name: MBP_Github_BlackduckSca_Test
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Project version: 1.3.0
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Integrated Matching Correlation ID: ad699102-9a62-4dc9-b79a-7333aa9ed167
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- BDIO Generated: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact/scan.bdio
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- No clone project or version name supplied. Will not clone.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- No project group was supplied. Will not assign a project group.
2025-11-03 19:37:42.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- No project version licenses were supplied.  Will not update licenses.
2025-11-03 19:37:45.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- No 'Application ID' to set.
2025-11-03 19:37:45.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- No custom fields to set.
2025-11-03 19:37:45.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Completed project and version actions.
2025-11-03 19:37:45.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Processing Detect Code Locations.
2025-11-03 19:37:46.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Scan initiated with scan service. Scan ID received: 7ef29aa9-1790-4034-a4ee-fdd81f3baffe
2025-11-03 19:37:46.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Successfully completed package manager scan of file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact/scan.bdio
2025-11-03 19:37:46.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Uploading scan.bdio
2025-11-03 19:37:48.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Starting the codelocation file uploads.
2025-11-03 19:37:48.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] DEBUG: --- Uploading BDIO file /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact/scan.bdio
2025-11-03 19:37:48.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] DEBUG: --- BDIO upload file count = 1
2025-11-03 19:37:48.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] DEBUG: --- Starting upload to https://saastest.app.blackduck.com/api/intelligent-persistence-scans/7ef29aa9-1790-4034-a4ee-fdd81f3baffe
2025-11-03 19:37:48.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] DEBUG: --- Appending file bdio-entry-00.jsonld, to https://saastest.app.blackduck.com/api/intelligent-persistence-scans/7ef29aa9-1790-4034-a4ee-fdd81f3baffe with count 1
2025-11-03 19:37:52.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] DEBUG: --- Finishing upload to https://saastest.app.blackduck.com/api/intelligent-persistence-scans/7ef29aa9-1790-4034-a4ee-fdd81f3baffe with count 1
2025-11-03 19:37:53.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] INFO: --- Try #1 for task bdio upload (elapsed: 00:00:00.000)...complete!
2025-11-03 19:37:53.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Completed the codelocation file uploads.
2025-11-03 19:37:53.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Completed Detect Code Location processing.
2025-11-03 19:37:53.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 19:37:53.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Signature Scanner tool.
2025-11-03 19:37:53.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Signature scanner will use the Black Duck SCA server to download/update the scanner - this is the most likely situation.
2025-11-03 19:37:53.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Using Tools Scan CLI download API (new).
2025-11-03 19:37:53.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- The directory structure was likely created by the installer
2025-11-03 19:37:53.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Locally installed signature scanner version: 1.0.6
2025-11-03 19:37:57.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Locally installed Signature Scanner version is up to date - skipping download.
2025-11-03 19:37:57.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- The directory structure was likely created by the installer
2025-11-03 19:37:58.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- The Black Duck Signature Scanner downloaded/found successfully: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools
2025-11-03 19:37:58.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- No scan targets provided - registering the source path /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm to scan
2025-11-03 19:38:00.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Starting the Black Duck Signature Scan commands.
2025-11-03 19:38:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] DEBUG: --- The directory structure was likely created by the installer
2025-11-03 19:38:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] DEBUG: --- Using this java installation : /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/jre/Contents/Home/bin/java
2025-11-03 19:38:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] DEBUG: --- Using the Black Duck hostname : 'saastest.app.blackduck.com'
2025-11-03 19:38:00.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- Black Duck CLI command: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/jre/Contents/Home/bin/java -Done-jar.silent=true -Done-jar.jar.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/lib/cache/scan.cli.impl-standalone.jar -Xmx4096m -jar /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/lib/scan.cli-1.0.6-standalone.jar --no-prompt --scheme https --host saastest.app.blackduck.com --port 443 -v --logDir /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1 --statusWriteDir /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1 --project MBP_Github_BlackduckSca_Test --release 1.3.0 --name nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature --exclude /node_modules/ --exclude /.bridge/ --scass-scan /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
2025-11-03 19:38:02.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Start wrapper: ScanCliWrapperSettings [commandLine=[args=[Ljava.lang.String;@3148f668, options=[Lorg.apache.commons.cli.Option;@6e005dc9], fileUriSet=null, scheme=https, host=saastest.app.blackduck.com, port=443]...
2025-11-03 19:38:02.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Start scan loop: ScanClientSettings [commandLine=[--no-prompt, --scheme, https, --host, saastest.app.blackduck.com, --port, 443, -v, --logDir, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1, --statusWriteDir, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1, --project, MBP_Github_BlackduckSca_Test, --release, 1.3.0, --name, nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature, --exclude, /node_modules/, --exclude, /.bridge/, --scass-scan, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm], fileUriSet=[file://BD-MB83224/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm], uploadCSV=false, dryRunWriteDir=No dry run file., outputFormat=null, scanId=null, dryRunReadFile=No dry run file., fsScanReadyWaitingPeriod=30, snippetMatching=false, snippetMatchingOnly=false, snippetMatchingAllSource=false, fullSnippetScan=false, uploadSource=false, individualFileMatching=none, licenseSearch=false, copyrightSearch=false, signatureGeneration=false, noSignatureGeneration=false, maxRequestBodySize=20000000, maxUpdateSize=10000, matchConfidenceThreshold=null, minScanInterval=null, logDir=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1, scheme=https, host=saastest.app.blackduck.com, port=443, name=Optional[nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature], project=Optional[MBP_Github_BlackduckSca_Test], release=Optional[1.3.0], username=null, password=<NOT SHOWN>, correlationId=null, noPersistence=false, noPersistenceMode=null, retainUnmatchedFiles=null, projectGroupName=null, scassScan=true]...
2025-11-03 19:38:02.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Individual File Matching Detected: none...
2025-11-03 19:38:02.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Finalized sha1 white list: []...
2025-11-03 19:38:02.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Finalized clean sha1 white list: []...
2025-11-03 19:38:02.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Initialize client for saastest.app.blackduck.com:443
2025-11-03 19:38:05.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Scan engine initialized with niceness set to false
2025-11-03 19:38:06.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Dry Run path: Optional.empty
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: ScanExecResult: ScanExecResult [scanClientSettings=ScanClientSettings [commandLine=[--no-prompt, --scheme, https, --host, saastest.app.blackduck.com, --port, 443, -v, --logDir, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1, --statusWriteDir, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1, --project, MBP_Github_BlackduckSca_Test, --release, 1.3.0, --name, nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature, --exclude, /node_modules/, --exclude, /.bridge/, --scass-scan, /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm], fileUriSet=[file://BD-MB83224/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm], uploadCSV=false, dryRunWriteDir=No dry run file., outputFormat=null, scanId=null, dryRunReadFile=No dry run file., fsScanReadyWaitingPeriod=30, snippetMatching=false, snippetMatchingOnly=false, snippetMatchingAllSource=false, fullSnippetScan=false, uploadSource=false, individualFileMatching=none, licenseSearch=false, copyrightSearch=false, signatureGeneration=false, noSignatureGeneration=false, maxRequestBodySize=20000000, maxUpdateSize=10000, matchConfidenceThreshold=null, minScanInterval=null, logDir=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1, scheme=https, host=saastest.app.blackduck.com, port=443, name=Optional[nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature], project=Optional[MBP_Github_BlackduckSca_Test], release=Optional[1.3.0], username=null, password=<NOT SHOWN>, correlationId=null, noPersistence=false, noPersistenceMode=null, retainUnmatchedFiles=null, projectGroupName=null, scassScan=true], result=0, dataFileName=2025_11_03_19_38_0512566677473499973965.tmp, scanContainer=null, sigGenScanContainer=SigGenScanContainerView{baseDir=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm, hostName=BD-MB83224, name=nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature, scannerVersion=1.0.6, signatureVersion=7.0.0, ownerEntityKeyToken=SN#BD-MB83224-nodejs-npm, createdOn=2025-11-03T14:08:05.720Z, timeToScan=179, scanNodeList.size()=30, scanLeafList.size()=105, scanProblem=null, scanProblemList.size()=0}, fpScanContainer=null, stringSearchScanContainer=null, scanResult=ScanView{id=4cb35e5f-e6c6-4304-9fdf-a50b177a0115, scannerVersion=1.0.6, signatureVersion=7.0.0, name=nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature, hostName=BD-MB83224, ownerEntityKeyToken=SN#BD-MB83224-nodejs-npm, baseDir=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm, createdOn=2025-11-03T14:08:05.720Z, matchCount=0, numDirs=0, numNonDirFiles=0, statusMessage=file://BD-MB83224/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm, deepSystemSize=Optional.empty, timeLastModified=0, timeToPersistMs=0, scanTime=0, arguments={}, debugMode=false}, scanSummary=ScanSummaryView{scanState=STARTED, transitionReason=SCAN_INGESTED, statusMessage=, createdAt=2025-11-03T14:08:05.985Z, updatedAt=2025-11-03T14:08:10.319Z, createdByUserName=Optional[sa_centralintegrations], scanSize=Optional[2972034], serverVersion=2025.7.1, matchCount=0, directoryCount=Optional[0], fileCount=Optional[0], baseDirectory=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm, hostName=BD-MB83224, scanType=SIGNATURE, errorCode=Optional.empty, retainUnmatchedFiles=false, resourceMetadata=MetaDataView{href=https://saastest.app.blackduck.com/api/scan-summaries/4cb35e5f-e6c6-4304-9fdf-a50b177a0115, links=[LinkView{rel=codelocation, href=https://saastest.app.blackduck.com/api/codelocations/0f1467b4-867f-498d-9341-a2c5738b6056}]}}, scanDate=Mon Nov 03 19:38:02 IST 2025, scanEndDate=Mon Nov 03 19:38:11 IST 2025, scanCreated=false, uploadUrl=null, uploadUrlData=null]
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Creating data output file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1/log/BD-MB83224-nodejs-npm-2025-11-03T140805.720Z.log
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Logging to file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1/log/BD-MB83224-nodejs-npm-2025-11-03T140805.720Z.log
2025-11-03 19:38:11.4652 IST [Blackduck SCA Detect Execution] INFO: Logging to file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1/log/BD-MB83224-nodejs-npm-2025-11-03T140805.720Z.log
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Persist scan output to file...
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Persisted status: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1/output/scanOutput.json
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Creating data output file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1/status/BD-MB83224-nodejs-npm-2025-11-03T140805.720Z.json
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1-Stream Redirect Thread] DEBUG: --- INFO: Persist ScanSummary to file...
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] DEBUG: --- INFO: Persisted status: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1/status/BD-MB83224-nodejs-npm-2025-11-03T140805.720Z.json
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- 
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- Black Duck Signature Scanner return code: 0
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- Signature Scanner log output directory: '/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1'
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Completed the Black Duck Signature Scan commands.
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Signature Scanner actions finished.
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Binary Scanner tool.
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Invoking intelligent persistent binary scan.
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Binary scanner found nothing to upload.
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Binary Scanner actions finished.
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Container Scanner tool.
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Invoking intelligent persistent container scan.
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Determining if configuration is valid to run a container scan.
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- No detect.container.scan.file.path property was provided. Skipping container scan.
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Container Scanner actions finished.
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Vulnerability Impact Analysis tool will not be run.
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- IaC Scanner tool will not be run.
2025-11-03 19:38:11.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 19:38:12.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #1 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/7ef29aa9-1790-4034-a4ee-fdd81f3baffe (elapsed: 00:00:00.000)...complete!
2025-11-03 19:38:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #1 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/4cb35e5f-e6c6-4304-9fdf-a50b177a0115 (elapsed: 00:00:00.000)...not done yet, waiting 1 seconds and trying again...
2025-11-03 19:38:15.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #2 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/4cb35e5f-e6c6-4304-9fdf-a50b177a0115 (elapsed: 00:00:01.923)...not done yet, waiting 2 seconds and trying again...
2025-11-03 19:38:18.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #3 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/4cb35e5f-e6c6-4304-9fdf-a50b177a0115 (elapsed: 00:00:04.851)...not done yet, waiting 3 seconds and trying again...
2025-11-03 19:38:22.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #4 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/4cb35e5f-e6c6-4304-9fdf-a50b177a0115 (elapsed: 00:00:08.924)...complete!
2025-11-03 19:38:22.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Checking to see if Detect should check policy for violations.
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Creating status file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-14-07-31-303/status/status.json
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][pool-2-thread-1] DEBUG: --- Starting phone home
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][pool-2-thread-1] DEBUG: --- Phoning home to https://www.google-analytics.com/mp/collect?api_secret=LA7cz8EKSLCmHdHdVdThGA&measurement_id=G-J4L8680QKM
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect shutdown begin.
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Finishing diagnostic mode.
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Finishing reports.
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Finishing logging.
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Finishing executable capture.
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Finishing file capture.
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Creating diagnostics zip.
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Diagnostics zip location: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/detect-run-2025-11-03-14-07-31-303.zip
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: status/status.json
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1/output/scanOutput.json
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1/status/BD-MB83224-nodejs-npm-2025-11-03T140805.720Z.json
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1/CLI_Output.txt
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: scan/BlackDuckScanOutput/2025-11-03_14-08-00-276_1/log/BD-MB83224-nodejs-npm-2025-11-03T140805.720Z.log
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: scan/.bdignore
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: logs/all.txt
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: logs/debug.txt
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: logs/info.txt
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: logs/sysout.txt
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: relevant/FILE-1-package.json
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: relevant/FILE-MAP.txt
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: relevant/FILE-0-package-lock.json
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/search_report.txt
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/detector_report.txt
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/dependency_counts_report.txt
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/search_detailed_report.txt
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/detect_configuration.txt
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/code_location_report.txt
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Adding file to zip: reports/detector_profile_report.txt
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Diagnostics file created at: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/detect-run-2025-11-03-14-07-31-303.zip
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Diagnostic mode has completed.
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Skipping cleanup, it is disabled.
2025-11-03 19:38:23.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Ending phone home.
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][pool-2-thread-1] DEBUG: --- Completed phone home
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Detect shutdown completed.
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- All Detect actions completed.
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- === Additional  Information ===
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- ====== Detect Operations ======
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Execute Detectors: SUCCESS
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- SubProject Aggregate: SUCCESS
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Package_manager Upload: SUCCESS
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Upload Intelligent Persistent Bdio: SUCCESS
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Create Online Signature Scan Batch: SUCCESS
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Execute Signature Scan CLI: SUCCESS
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- Retrieve Container Scan Image File: SUCCESS
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- ===============================
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] DEBUG: --- 
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======== Detect Result ========
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Black Duck SCA Project BOM: https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/components
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======== Detect Status ========
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- NPM: SUCCESS
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Signature scan / Snippet scan on /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm: SUCCESS
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Overall Status: SUCCESS - Detect exited successfully.
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ===============================
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 19:38:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect duration: 00h 00m 58s 141ms
2025-11-03 19:38:24.9237 IST [Blackduck SCA Detect Execution] INFO: Provided value for resource 'detect.completed'
2025-11-03 19:38:24.9237 IST [Blackduck SCA Detect Execution] DEBUG: Provided value 'true' for resource 'detect.completed'
2025-11-03 19:38:24.9238 IST [Blackduck SCA Detect Execution] INFO: Provided value for resource 'detect.results.path'
2025-11-03 19:38:24.9239 IST [Blackduck SCA Detect Execution] DEBUG: Provided value '/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect' for resource 'detect.results.path'
2025-11-03 19:38:24.9243 IST [Blackduck SCA Detect Execution] INFO: Adapter finished
2025-11-03 19:38:24.9783 IST [Blackduck SCA Results] INFO: Skipping Blackduck SCA issues retrieval as "blackducksca.fixpr.enabled" is configured to false
2025-11-03 19:38:24.9836 IST [Blackduck SCA Results] INFO: Adapter finished
2025-11-03 19:38:25.0304 IST [SCM Checker] DEBUG: JENKINS_HOME is set to value: "/Users/madhusud/.jenkins"
2025-11-03 19:38:25.0356 IST [SCM Checker] INFO: Provided value for resource 'jenkins.enabled'
2025-11-03 19:38:25.0356 IST [SCM Checker] DEBUG: Provided value 'true' for resource 'jenkins.enabled'
2025-11-03 19:38:25.0356 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-policy-violations-fetcher
2025-11-03 19:38:25.0361 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Policy Violations Fetcher
2025-11-03 19:38:25.0362 IST [SCM Checker] INFO: Adapter finished
2025-11-03 19:38:25.0840 IST [Detect Component Locator] INFO: skipping fix pull requests creation as "blackducksca.fixpr.enabled" is configured to false
2025-11-03 19:38:25.0891 IST [Detect Component Locator] INFO: Adapter finished
2025-11-03 19:38:25.1355 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Jenkins is enabled
2025-11-03 19:38:25.1357 IST [Blackduck SCA Policy Violations Fetcher] INFO: Detected Intelligent scan, will fetch Intelligent scan policy violations data
2025-11-03 19:38:26.3480 IST [Blackduck SCA Policy Violations Fetcher] INFO: Bearer token retrieved successfully
2025-11-03 19:38:26.7341 IST [Blackduck SCA Policy Violations Fetcher] INFO: Project data retrieved successfully
2025-11-03 19:38:27.1408 IST [Blackduck SCA Policy Violations Fetcher] INFO: Version data retrieved successfully
2025-11-03 19:38:27.5478 IST [Blackduck SCA Policy Violations Fetcher] INFO: Detected 5 policy violations
2025-11-03 19:38:27.9548 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: BOM Policy Violations Status: [{BLOCKER 1095} {CRITICAL 0} {MAJOR 0} {MINOR 0} {TRIVIAL 0} {UNSPECIFIED 0} {OK 0}]
2025-11-03 19:38:27.9763 IST [Blackduck SCA Policy Violations Fetcher] INFO: Added entry to resource 'blackducksca.policy.rules.violations'
2025-11-03 19:38:27.9763 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/components?filter=policyRuleSeverity:BLOCKER&filter=policyRuleViolation:PR~703321de-2390-42af-96dd-c9446f5074b8' to resource 'blackducksca.policy.rules.violations.[0].referenceUrl'
2025-11-03 19:38:27.9763 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'all_components_vulns' to resource 'blackducksca.policy.rules.violations.[0].policyName'
2025-11-03 19:38:27.9763 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry '1092' to resource 'blackducksca.policy.rules.violations.[0].bomViolationCount'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'BLOCKER' to resource 'blackducksca.policy.rules.violations.[0].policySeverity'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'all_match_types' to resource 'blackducksca.policy.rules.violations.[1].policyName'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry '1092' to resource 'blackducksca.policy.rules.violations.[1].bomViolationCount'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'BLOCKER' to resource 'blackducksca.policy.rules.violations.[1].policySeverity'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/components?filter=policyRuleSeverity:BLOCKER&filter=policyRuleViolation:PR~aaba247e-58a7-46fa-b089-018e9fade98b' to resource 'blackducksca.policy.rules.violations.[1].referenceUrl'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'all_security_vulns' to resource 'blackducksca.policy.rules.violations.[2].policyName'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry '139' to resource 'blackducksca.policy.rules.violations.[2].bomViolationCount'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'BLOCKER' to resource 'blackducksca.policy.rules.violations.[2].policySeverity'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/components?filter=policyRuleSeverity:BLOCKER&filter=policyRuleViolation:PR~057d51ea-542c-4f90-8e65-4612ff318bdb' to resource 'blackducksca.policy.rules.violations.[2].referenceUrl'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry '63' to resource 'blackducksca.policy.rules.violations.[3].bomViolationCount'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'CRITICAL' to resource 'blackducksca.policy.rules.violations.[3].policySeverity'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/components?filter=policyRuleSeverity:CRITICAL&filter=policyRuleViolation:PR~833ce858-fe66-419e-b0a5-f1d1012e22b1' to resource 'blackducksca.policy.rules.violations.[3].referenceUrl'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'Critical_With Overall_Score_GE 7' to resource 'blackducksca.policy.rules.violations.[3].policyName'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'Operational_Risk_With_Match_Type' to resource 'blackducksca.policy.rules.violations.[4].policyName'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry '2' to resource 'blackducksca.policy.rules.violations.[4].bomViolationCount'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'MAJOR' to resource 'blackducksca.policy.rules.violations.[4].policySeverity'
2025-11-03 19:38:27.9764 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Added entry 'https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/components?filter=policyRuleSeverity:MAJOR&filter=policyRuleViolation:PR~79645908-f677-4163-a8dd-cf85f746830b' to resource 'blackducksca.policy.rules.violations.[4].referenceUrl'
2025-11-03 19:38:27.9766 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.trivial'
2025-11-03 19:38:27.9766 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Provided value '0' for resource 'blackducksca.policy.status.issues.trivial'
2025-11-03 19:38:27.9768 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.unspecified'
2025-11-03 19:38:27.9768 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Provided value '0' for resource 'blackducksca.policy.status.issues.unspecified'
2025-11-03 19:38:27.9770 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.major'
2025-11-03 19:38:27.9770 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Provided value '0' for resource 'blackducksca.policy.status.issues.major'
2025-11-03 19:38:27.9772 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.ok'
2025-11-03 19:38:27.9772 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Provided value '0' for resource 'blackducksca.policy.status.issues.ok'
2025-11-03 19:38:27.9774 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.critical'
2025-11-03 19:38:27.9774 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Provided value '0' for resource 'blackducksca.policy.status.issues.critical'
2025-11-03 19:38:27.9776 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.blocker'
2025-11-03 19:38:27.9776 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Provided value '1095' for resource 'blackducksca.policy.status.issues.blocker'
2025-11-03 19:38:27.9777 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.minor'
2025-11-03 19:38:27.9777 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Provided value '0' for resource 'blackducksca.policy.status.issues.minor'
2025-11-03 19:38:27.9779 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.projectBomUrl'
2025-11-03 19:38:27.9779 IST [Blackduck SCA Policy Violations Fetcher] DEBUG: Provided value 'https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/components' for resource 'blackducksca.projectBomUrl'
2025-11-03 19:38:27.9788 IST [Blackduck SCA Policy Violations Fetcher] INFO: Adapter finished
******************************* END EXECUTION OF BRIDGE CLI *******************************
[Security Scan] INFO: Archiving DIAGNOSTIC jenkins artifact from: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge
Archiving artifacts
[Security Scan] INFO: DIAGNOSTIC archived successfully in jenkins artifact
[Security Scan] INFO: Retrieving the issue count from the scan results
[Security Scan] INFO: Total issues found: 1095
[Security Scan] INFO: Security Scan execution is successful
[Security Scan] INFO: Marking build status as FAILURE is ignored since exit code is: 0
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
Build Number: 40
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