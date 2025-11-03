# Jenkins Execution Log

## Build Information
- **Job Name:** `MBP_Github_BlackduckSca_Test/main`
- **Build Number:** #46
- **Build Status:** 🟢 **SUCCESS**
- **Duration:** 4 min 14 sec and counting
- **Timestamp:** 2025-11-03 21:52:30 UTC

---

## Console Output

```
Started by user admin
Connecting to https://api.github.com using madhusud@blackduck.com/****** (Github_Username_PAT)
Obtained nodejs-npm/Jenkinsfile from db05fca081961e2d34c5dbb220cf2af4209f6d75
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
Checking out Revision db05fca081961e2d34c5dbb220cf2af4209f6d75 (main)
 > git config core.sparsecheckout # timeout=10
Commit message: "Jenkins log upload - Build #45"
 > git checkout -f db05fca081961e2d34c5dbb220cf2af4209f6d75 # timeout=10
 > git rev-list --no-walk 6ff4e4c17dc29841e9fd20b593e78b8b72955139 # timeout=10
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
[Security Scan] INFO:  --- mark_build_status = FAILURE
[Security Scan] INFO:  --- network_airgap = false
[Security Scan] INFO: Black Duck SCA parameters are validated successfully
[Security Scan] INFO: Bridge download parameters are validated successfully
[Security Scan] INFO: Bridge download is not required. Found installed in: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
------------------------------------------------------------------------------------
[Security Scan] INFO: Bridge CLI version is - 3.9.2
[Security Scan] INFO: Jenkins Job name: MBP_Github_BlackduckSca_Test
[Security Scan] INFO: Jenkins Job name: MBP_Github_BlackduckSca_Test
[Security Scan] INFO: Executable command line arguments: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm/bridge-cli --stage blackducksca --input /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/blackducksca_input6625596080585252350.json --out .bridge/output/scan_info_out.json

******************************* START EXECUTION OF BRIDGE CLI *******************************
2025-11-03 21:51:27.5138 IST [Bridge CLI] INFO: Using cache directory: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
2025-11-03 21:51:27.5215 IST [Bridge CLI] INFO: Found version "3.0.143" in registry for workflow "blackducksca", trying to load it from local cache
2025-11-03 21:51:27.6425 IST [Bridge CLI] INFO: Input Resources:
2025-11-03 21:51:27.6425 IST [Bridge CLI] INFO: resource = value [source]
2025-11-03 21:51:27.6425 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-03 21:51:27.6425 IST [Bridge CLI] INFO: blackducksca.scan.full = true [blackducksca_input6625596080585252350.json]
2025-11-03 21:51:27.6426 IST [Bridge CLI] INFO: blackducksca.token = ***************************************** [blackducksca_input6625596080585252350.json]
2025-11-03 21:51:27.6426 IST [Bridge CLI] INFO: blackducksca.url = https://saastest.app.blackduck.com [blackducksca_input6625596080585252350.json]
2025-11-03 21:51:27.6426 IST [Bridge CLI] INFO: blackducksca.waitForScan = true [blackducksca_input6625596080585252350.json]
2025-11-03 21:51:27.6426 IST [Bridge CLI] INFO: network.airgap = false [blackducksca_input6625596080585252350.json]
2025-11-03 21:51:27.6426 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-03 21:51:27.6426 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca
2025-11-03 21:51:27.6429 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Controller
2025-11-03 21:51:27.6506 IST [Bridge CLI] INFO: Starting Adapter: Check pull request
2025-11-03 21:51:27.6823 IST [Check pull request] INFO: Provided value for resource 'environment.scan.pull'
2025-11-03 21:51:27.6826 IST [Check pull request] INFO: Adapter finished
2025-11-03 21:51:28.7046 IST [Blackduck SCA Controller] INFO: Found Black Duck SCA Detect jar file "detect-11.0.0.jar" in "/Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0"
2025-11-03 21:51:28.7266 IST [Blackduck SCA Controller] INFO: Provided value for resource 'detect.execution.path'
2025-11-03 21:51:28.7267 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-detect
2025-11-03 21:51:28.7268 IST [Bridge CLI] INFO: Starting adapters for stage scm
2025-11-03 21:51:28.7268 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-post-processing
2025-11-03 21:51:28.7308 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Results
2025-11-03 21:51:28.7308 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Detect Execution
2025-11-03 21:51:28.7308 IST [Bridge CLI] INFO: Starting Adapter: Detect Component Locator
2025-11-03 21:51:28.7308 IST [Bridge CLI] INFO: Starting Adapter: SCM Checker
2025-11-03 21:51:28.7313 IST [Blackduck SCA Controller] INFO: Adapter finished
2025-11-03 21:51:28.7996 IST [Blackduck SCA Detect Execution] INFO: Running command /Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home/bin/java -jar /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0/detect-11.0.0.jar --detect.cleanup=false --detect.bdio.file.name=scan --detect.bdio.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact --detect.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect --blackduck.offline.mode=false --blackduck.url=https://saastest.app.blackduck.com --blackduck.api.token= --detect.wait.for.results=true --detect.blackduck.scan.mode=INTELLIGENT
2025-11-03 21:51:29.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect-Self-Updater:  Checking https://saastest.app.blackduck.com/api/tools/detect API for centrally managed Detect version to download to /Users/madhusud/tmp.
2025-11-03 21:51:32.0000 IST [Blackduck SCA Detect Execution][main] WARNING: --- Detect-Self-Updater:  Unable to download jar from https://saastest.app.blackduck.com/api/tools/detect.
2025-11-03 21:51:32.0000 IST [Blackduck SCA Detect Execution][main] WARNING: --- Detect-Self-Updater:  Response code from https://saastest.app.blackduck.com/api/tools/detect was: 400 Bad Request
2025-11-03 21:51:33.2826 IST [Blackduck SCA Detect Execution] INFO: ______     _            _
2025-11-03 21:51:33.2827 IST [Blackduck SCA Detect Execution] INFO: |  _  \   | |          | |
2025-11-03 21:51:33.2827 IST [Blackduck SCA Detect Execution] INFO: | | | |___| |_ ___  ___| |_
2025-11-03 21:51:33.2827 IST [Blackduck SCA Detect Execution] INFO: | | | / _ \ __/ _ \/ __| __|
2025-11-03 21:51:33.2827 IST [Blackduck SCA Detect Execution] INFO: | |/ /  __/ ||  __/ (__| |_
2025-11-03 21:51:33.2827 IST [Blackduck SCA Detect Execution] INFO: |___/ \___|\__\___|\___|\__|
2025-11-03 21:51:33.2827 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-03 21:51:33.3812 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-03 21:51:33.3813 IST [Blackduck SCA Detect Execution] INFO: Detect Version: 11.0.0
2025-11-03 21:51:33.3813 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Current property values:
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- --property = value [notes]
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ------------------------------------------------------------
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.api.token = **************************************************************************************************** [cmd] 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.offline.mode = false [cmd] 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.url = https://saastest.app.blackduck.com [cmd] 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.bdio.file.name = scan [cmd] 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.bdio.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact [cmd] 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.blackduck.scan.mode = INTELLIGENT [cmd] 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.cleanup = false [cmd] 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.excluded.directories = /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge [env] 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect [cmd] 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.project.name = MBP_Github_BlackduckSca_Test [env] 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.wait.for.results = true [cmd] 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ------------------------------------------------------------
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect build date: 2025-10-30
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Source directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Output directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Run directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-21-33-372
2025-11-03 21:51:33.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:51:41.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Successfully connected to Black Duck SCA (version 2025.7.1)!
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Docker tool.
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Docker actions finished.
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Bazel tool.
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Bazel actions finished.
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Detectors tool.
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Searching for detectors.
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Evaluating detectors. This may take a while.
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======================================================================================================
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detector Report
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======================================================================================================
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 	/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm (depth 0)
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 		NPM Package Lock: SUCCESS
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package-lock.json
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 			Found file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/package.json
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detectors actions finished.
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Project name: MBP_Github_BlackduckSca_Test
2025-11-03 21:51:43.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Project version: 1.3.0
2025-11-03 21:51:47.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Successfully completed package manager scan of file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact/scan.bdio
2025-11-03 21:51:50.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Starting the codelocation file uploads.
2025-11-03 21:51:55.0000 IST [Blackduck SCA Detect Execution][pool-1-thread-1] INFO: --- Try #1 for task bdio upload (elapsed: 00:00:00.000)...complete!
2025-11-03 21:51:55.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Completed the codelocation file uploads.
2025-11-03 21:51:55.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:51:55.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Signature Scanner tool.
2025-11-03 21:51:59.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- The Black Duck Signature Scanner downloaded/found successfully: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools
2025-11-03 21:51:59.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- No scan targets provided - registering the source path /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm to scan
2025-11-03 21:52:02.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Starting the Black Duck Signature Scan commands.
2025-11-03 21:52:02.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- Black Duck CLI command: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/jre/Contents/Home/bin/java -Done-jar.silent=true -Done-jar.jar.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/lib/cache/scan.cli.impl-standalone.jar -Xmx4096m -jar /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/tools/Black_Duck_Scan_Installation/scan.cli-1.0.6/lib/scan.cli-1.0.6-standalone.jar --no-prompt --scheme https --host saastest.app.blackduck.com --port 443 -v --logDir /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-21-33-372/scan/BlackDuckScanOutput/2025-11-03_16-22-02-227_1 --statusWriteDir /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-21-33-372/scan/BlackDuckScanOutput/2025-11-03_16-22-02-227_1 --project MBP_Github_BlackduckSca_Test --release 1.3.0 --name nodejs-npm/MBP_Github_BlackduckSca_Test/1.3.0 signature --exclude /node_modules/ --exclude /.bridge/ --scass-scan /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- 
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- Black Duck Signature Scanner return code: 0
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][pool-3-thread-1] INFO: --- Signature Scanner log output directory: '/Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-21-33-372/scan/BlackDuckScanOutput/2025-11-03_16-22-02-227_1'
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Completed the Black Duck Signature Scan commands.
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Signature Scanner actions finished.
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Binary Scanner tool.
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Binary scanner found nothing to upload.
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Binary Scanner actions finished.
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Will include the Container Scanner tool.
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- No detect.container.scan.file.path property was provided. Skipping container scan.
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Container Scanner actions finished.
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Vulnerability Impact Analysis tool will not be run.
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- IaC Scanner tool will not be run.
2025-11-03 21:52:13.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ----------------------------------
2025-11-03 21:52:14.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #1 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/199b4e6c-35a0-4a8c-b955-657f399a5d5b (elapsed: 00:00:00.000)...complete!
2025-11-03 21:52:15.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #1 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/fdad7b1b-a681-41e4-b093-d0f0474f1978 (elapsed: 00:00:00.000)...not done yet, waiting 1 seconds and trying again...
2025-11-03 21:52:17.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #2 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/fdad7b1b-a681-41e4-b093-d0f0474f1978 (elapsed: 00:00:01.947)...not done yet, waiting 2 seconds and trying again...
2025-11-03 21:52:20.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #3 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/fdad7b1b-a681-41e4-b093-d0f0474f1978 (elapsed: 00:00:04.862)...not done yet, waiting 3 seconds and trying again...
2025-11-03 21:52:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Try #4 for task BOM Scan Wait Job https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/bom-status/fdad7b1b-a681-41e4-b093-d0f0474f1978 (elapsed: 00:00:08.767)...complete!
2025-11-03 21:52:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Checking to see if Detect should check policy for violations.
2025-11-03 21:52:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:52:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:52:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Creating status file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-03-16-21-33-372/status/status.json
2025-11-03 21:52:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:52:24.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Skipping cleanup, it is disabled.
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======== Detect Result ========
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Black Duck SCA Project BOM: https://saastest.app.blackduck.com/api/projects/445f8925-3a9e-4dd6-9ca7-0bf6fdfca8e2/versions/16d2b091-a3e9-4176-9084-819db8e5fc0e/components
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======== Detect Status ========
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- NPM: SUCCESS
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Signature scan / Snippet scan on /Users/madhusud/Jenkins_Testing/Nodes/workspace/BP_Github_BlackduckSca_Test_main/nodejs-npm: SUCCESS
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Overall Status: SUCCESS - Detect exited successfully.
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ===============================
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-03 21:52:26.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect duration: 00h 00m 56s 710ms
2025-11-03 21:52:26.0758 IST [Blackduck SCA Detect Execution] INFO: Provided value for resource 'detect.completed'
2025-11-03 21:52:26.0760 IST [Blackduck SCA Detect Execution] INFO: Provided value for resource 'detect.results.path'
2025-11-03 21:52:26.0763 IST [Blackduck SCA Detect Execution] INFO: Adapter finished
2025-11-03 21:52:26.1235 IST [Blackduck SCA Results] INFO: Skipping Blackduck SCA issues retrieval as "blackducksca.fixpr.enabled" is configured to false
2025-11-03 21:52:26.1309 IST [Blackduck SCA Results] INFO: Adapter finished
2025-11-03 21:52:26.1794 IST [SCM Checker] INFO: Provided value for resource 'jenkins.enabled'
2025-11-03 21:52:26.1795 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-policy-violations-fetcher
2025-11-03 21:52:26.1799 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Policy Violations Fetcher
2025-11-03 21:52:26.1800 IST [SCM Checker] INFO: Adapter finished
2025-11-03 21:52:26.2137 IST [Detect Component Locator] INFO: skipping fix pull requests creation as "blackducksca.fixpr.enabled" is configured to false
2025-11-03 21:52:26.2184 IST [Detect Component Locator] INFO: Adapter finished
2025-11-03 21:52:26.2449 IST [Blackduck SCA Policy Violations Fetcher] INFO: Detected Intelligent scan, will fetch Intelligent scan policy violations data
2025-11-03 21:52:27.4679 IST [Blackduck SCA Policy Violations Fetcher] INFO: Bearer token retrieved successfully
2025-11-03 21:52:27.8868 IST [Blackduck SCA Policy Violations Fetcher] INFO: Project data retrieved successfully
2025-11-03 21:52:28.3016 IST [Blackduck SCA Policy Violations Fetcher] INFO: Version data retrieved successfully
2025-11-03 21:52:28.7209 IST [Blackduck SCA Policy Violations Fetcher] INFO: Detected 5 policy violations
2025-11-03 21:52:29.1761 IST [Blackduck SCA Policy Violations Fetcher] INFO: Added entry to resource 'blackducksca.policy.rules.violations'
2025-11-03 21:52:29.1763 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.minor'
2025-11-03 21:52:29.1764 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.trivial'
2025-11-03 21:52:29.1766 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.critical'
2025-11-03 21:52:29.1767 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.blocker'
2025-11-03 21:52:29.1768 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.major'
2025-11-03 21:52:29.1769 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.ok'
2025-11-03 21:52:29.1770 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.policy.status.issues.unspecified'
2025-11-03 21:52:29.1771 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.projectBomUrl'
2025-11-03 21:52:29.1775 IST [Blackduck SCA Policy Violations Fetcher] INFO: Adapter finished
******************************* END EXECUTION OF BRIDGE CLI *******************************
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
Build Number: 46
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