# Jenkins Execution Log

## Build Information
- **Job Name:** `MBP_Github_Polaris_Build_Scan/main`
- **Build Number:** #1
- **Build Status:** 🔴 **FAILURE**
- **Duration:** 37 sec and counting
- **Timestamp:** 2025-11-13 11:25:08 UTC

---

## Console Output

```
Branch indexing
Connecting to https://api.github.com using madhusud@blackduck.com/****** (Github_Username_PAT)
Obtained nodejs-npm/Jenkinsfile from ec0ab58a26b737ee90fe510da9fc74598f003cb2
Loading library blackduck-logs-publisher@main
Attempting to resolve main from remote references...
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git ls-remote -h -- https://github.com/integrations-garage/blackduck-logs-publisher # timeout=10
Found match: refs/heads/main revision e969196a63b1be83b84541b022f7aa52928bd5e5
The recommended git tool is: NONE
using credential Github_Username_PAT
Cloning the remote Git repository
Cloning with configured refspecs honoured and without tags
Cloning repository https://github.com/integrations-garage/blackduck-logs-publisher
 > git init /Users/madhusud/.jenkins/workspace/P_Github_Polaris_Build_Scan_main@libs/a0dda568bac7bbb4a171f59ba3f2660c21c69edc6356524e9ae8bb4500c12bbb # timeout=10
Fetching upstream changes from https://github.com/integrations-garage/blackduck-logs-publisher
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git fetch --no-tags --force --progress -- https://github.com/integrations-garage/blackduck-logs-publisher +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git config remote.origin.url https://github.com/integrations-garage/blackduck-logs-publisher # timeout=10
 > git config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
Avoid second fetch
Checking out Revision e969196a63b1be83b84541b022f7aa52928bd5e5 (main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f e969196a63b1be83b84541b022f7aa52928bd5e5 # timeout=10
Commit message: "Phase 3 - 2"
First time build. Skipping changelog.
[Pipeline] Start of Pipeline
[Pipeline] node
Running on mac-sh in /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Checkout SCM)
[Pipeline] checkout
The recommended git tool is: NONE
using credential Github_Username_PAT
Cloning the remote Git repository
Cloning with configured refspecs honoured and without tags
Cloning repository https://github.com/blackducksca-jenkins-samples/full-scan.git
 > git init /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main # timeout=10
Fetching upstream changes from https://github.com/blackducksca-jenkins-samples/full-scan.git
 > git --version # timeout=10
 > git --version # 'git version 2.39.5 (Apple Git-154)'
using GIT_ASKPASS to set credentials Github_Username_PAT
 > git fetch --no-tags --force --progress -- https://github.com/blackducksca-jenkins-samples/full-scan.git +refs/heads/main:refs/remotes/origin/main # timeout=10
Avoid second fetch
Checking out Revision ec0ab58a26b737ee90fe510da9fc74598f003cb2 (main)
Commit message: "Jenkins log cleanup - removing old log file"
First time build. Skipping changelog.
 > git config remote.origin.url https://github.com/blackducksca-jenkins-samples/full-scan.git # timeout=10
 > git config --add remote.origin.fetch +refs/heads/main:refs/remotes/origin/main # timeout=10
 > git config core.sparsecheckout # timeout=10
 > git checkout -f ec0ab58a26b737ee90fe510da9fc74598f003cb2 # timeout=10
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Build)
[Pipeline] script
[Pipeline] {
[Pipeline] echo
JOB_NAME: MBP_Github_Polaris_Build_Scan/main
[Pipeline] dir
Running in /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main/nodejs-npm
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
npm warn deprecated set-value@2.0.0: Critical bug fixed in v3.0.1, please upgrade to the latest version.
npm warn deprecated mixin-deep@1.3.1: Critical bug fixed in v2.0.1, please upgrade to the latest version.
npm warn deprecated ini@1.3.5: Please update to ini >=1.3.6 to avoid a prototype pollution issue
npm warn deprecated set-value@0.4.3: Critical bug fixed in v3.0.1, please upgrade to the latest version.
npm warn deprecated path-is-absolute@2.0.0: This package is no longer relevant as Node.js 0.12 is unmaintained.
npm warn deprecated urix@0.1.0: Please see https://github.com/lydell/urix#deprecated
npm warn deprecated har-validator@5.1.3: this library is no longer supported
npm warn deprecated to-iso-string@0.0.2: to-iso-string has been deprecated, use @segment/to-iso-string instead.
npm warn deprecated cryptiles@2.0.5: This version has been deprecated in accordance with the hapi support policy (hapi.im/support). Please upgrade to the latest version to get the best features, bug fixes, and security patches. If you are unable to upgrade at this time, paid support is available for older versions (hapi.im/commercial).
npm warn deprecated resolve-url@0.2.1: https://github.com/lydell/resolve-url#deprecated
npm warn deprecated bcrypt-nodejs@0.0.3: bcrypt-nodejs is no longer actively maintained. Please use bcrypt or bcryptjs. See https://github.com/kelektiv/node.bcrypt.js/wiki/bcrypt-vs-brypt.js to learn more about these two options
npm warn deprecated cryptiles@0.2.2: This version has been deprecated in accordance with the hapi support policy (hapi.im/support). Please upgrade to the latest version to get the best features, bug fixes, and security patches. If you are unable to upgrade at this time, paid support is available for older versions (hapi.im/commercial).
npm warn deprecated source-map-url@0.4.0: See https://github.com/lydell/source-map-url#deprecated
npm warn deprecated boom@0.4.2: This version has been deprecated in accordance with the hapi support policy (hapi.im/support). Please upgrade to the latest version to get the best features, bug fixes, and security patches. If you are unable to upgrade at this time, paid support is available for older versions (hapi.im/commercial).
npm warn deprecated debug@3.2.6: Debug versions >=3.2.0 <3.2.7 || >=4 <4.3.1 have a low-severity ReDos regression when used in a Node.js environment. It is recommended you upgrade to 3.2.7 or 4.3.1. (https://github.com/visionmedia/debug/issues/797)
npm warn deprecated debug@3.2.6: Debug versions >=3.2.0 <3.2.7 || >=4 <4.3.1 have a low-severity ReDos regression when used in a Node.js environment. It is recommended you upgrade to 3.2.7 or 4.3.1. (https://github.com/visionmedia/debug/issues/797)
npm warn deprecated debug@3.2.6: Debug versions >=3.2.0 <3.2.7 || >=4 <4.3.1 have a low-severity ReDos regression when used in a Node.js environment. It is recommended you upgrade to 3.2.7 or 4.3.1. (https://github.com/visionmedia/debug/issues/797)
npm warn deprecated debug@3.2.6: Debug versions >=3.2.0 <3.2.7 || >=4 <4.3.1 have a low-severity ReDos regression when used in a Node.js environment. It is recommended you upgrade to 3.2.7 or 4.3.1. (https://github.com/visionmedia/debug/issues/797)
npm warn deprecated boom@2.10.1: This version has been deprecated in accordance with the hapi support policy (hapi.im/support). Please upgrade to the latest version to get the best features, bug fixes, and security patches. If you are unable to upgrade at this time, paid support is available for older versions (hapi.im/commercial).
npm warn deprecated chokidar@2.1.6: Chokidar 2 does not receive security updates since 2019. Upgrade to chokidar 3 with 15x fewer dependencies
npm warn deprecated sntp@0.2.4: This module moved to @hapi/sntp. Please make sure to switch over as this distribution is no longer supported and may contain bugs and critical security issues.
npm warn deprecated minimatch@0.3.0: Please update to minimatch 3.0.2 or higher to avoid a RegExp DoS issue
npm warn deprecated chokidar@2.1.8: Chokidar 2 does not receive security updates since 2019. Upgrade to chokidar 3 with 15x fewer dependencies
npm warn deprecated sntp@1.0.9: This module moved to @hapi/sntp. Please make sure to switch over as this distribution is no longer supported and may contain bugs and critical security issues.
npm warn deprecated querystring@0.2.0: The querystring API is considered Legacy. new code should use the URLSearchParams API instead.
npm warn deprecated request@2.36.0: request has been deprecated, see https://github.com/request/request/issues/3142
npm warn deprecated mkdirp@0.3.0: Legacy versions of mkdirp are no longer supported. Please update to mkdirp 1.x. (Note that the API surface has changed to use Promises in 1.x.)
npm warn deprecated tough-cookie@2.2.2: ReDoS vulnerability parsing Set-Cookie https://nodesecurity.io/advisories/130
npm warn deprecated hoek@0.9.1: This version has been deprecated in accordance with the hapi support policy (hapi.im/support). Please upgrade to the latest version to get the best features, bug fixes, and security patches. If you are unable to upgrade at this time, paid support is available for older versions (hapi.im/commercial).
npm warn deprecated node-uuid@1.4.8: Use uuid module instead
npm warn deprecated node-uuid@1.4.8: Use uuid module instead
npm warn deprecated uuid@3.3.2: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm warn deprecated source-map-resolve@0.5.2: See https://github.com/lydell/source-map-resolve#deprecated
npm warn deprecated har-validator@2.0.6: this library is no longer supported
npm warn deprecated mkdirp@0.5.1: Legacy versions of mkdirp are no longer supported. Please update to mkdirp 1.x. (Note that the API surface has changed to use Promises in 1.x.)
npm warn deprecated hoek@2.16.3: This version has been deprecated in accordance with the hapi support policy (hapi.im/support). Please upgrade to the latest version to get the best features, bug fixes, and security patches. If you are unable to upgrade at this time, paid support is available for older versions (hapi.im/commercial).
npm warn deprecated request@2.79.0: request has been deprecated, see https://github.com/request/request/issues/3142
npm warn deprecated request@2.88.0: request has been deprecated, see https://github.com/request/request/issues/3142
npm warn deprecated request@2.67.0: request has been deprecated, see https://github.com/request/request/issues/3142
npm warn deprecated readdir-scoped-modules@1.0.2: This functionality has been moved to @npmcli/fs
npm warn deprecated hawk@1.0.0: This module moved to @hapi/hawk. Please make sure to switch over as this distribution is no longer supported and may contain bugs and critical security issues.
npm warn deprecated hawk@3.1.3: This module moved to @hapi/hawk. Please make sure to switch over as this distribution is no longer supported and may contain bugs and critical security issues.
npm warn deprecated jade@0.26.3: Jade has been renamed to pug, please install the latest version of pug instead of jade
npm warn deprecated swig@1.4.2: This package is no longer maintained
npm warn deprecated bson@1.0.9: Fixed a critical issue with BSON serialization documented in CVE-2019-2391, see https://bit.ly/2KcpXdo for more details
npm warn deprecated nodeunit@0.9.5: you are strongly encouraged to use other testing options

added 962 packages, and audited 1412 packages in 15s

32 packages are looking for funding
  run `npm fund` for details

136 vulnerabilities (9 low, 35 moderate, 57 high, 35 critical)

To address issues that do not require attention, run:
  npm audit fix

To address all issues possible (including breaking changes), run:
  npm audit fix --force

Some issues need review, and may require choosing
a different dependency.

Run `npm audit` for details.
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
Running in /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main/nodejs-npm
[Pipeline] {
[Pipeline] echo
DETECT_PROJECT_NAME will be set to: MBP_Github_Polaris_Build_Scan
[Pipeline] withEnv
[Pipeline] {
[Pipeline] security_scan
**************************** START EXECUTION OF BLACK DUCK SECURITY SCAN ****************************
[Security Scan] INFO: Jenkins Job name: MBP_Github_Polaris_Build_Scan
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
[Security Scan] INFO: Jenkins Job name: MBP_Github_Polaris_Build_Scan
[Security Scan] INFO: Jenkins Job name: MBP_Github_Polaris_Build_Scan
[Security Scan] INFO: Executable command line arguments: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm/bridge-cli --stage blackducksca --input /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main/blackducksca_input8761691229404563484.json --out .bridge/output/scan_info_out.json

******************************* START EXECUTION OF BRIDGE CLI *******************************
2025-11-13 11:25:01.9041 IST [Bridge CLI] INFO: Using cache directory: /Users/madhusud/bridge-cli-bundle/bridge-cli-bundle-macos_arm
2025-11-13 11:25:01.9136 IST [Bridge CLI] INFO: Found version "3.0.143" in registry for workflow "blackducksca", trying to load it from local cache
2025-11-13 11:25:02.0190 IST [Bridge CLI] INFO: Input Resources:
2025-11-13 11:25:02.0191 IST [Bridge CLI] INFO: resource = value [source]
2025-11-13 11:25:02.0191 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-13 11:25:02.0191 IST [Bridge CLI] INFO: blackducksca.scan.full = true [blackducksca_input8761691229404563484.json]
2025-11-13 11:25:02.0191 IST [Bridge CLI] INFO: blackducksca.token = ***************************************** [blackducksca_input8761691229404563484.json]
2025-11-13 11:25:02.0191 IST [Bridge CLI] INFO: blackducksca.url = https://saastest.app.blackduck.com [blackducksca_input8761691229404563484.json]
2025-11-13 11:25:02.0191 IST [Bridge CLI] INFO: blackducksca.waitForScan = true [blackducksca_input8761691229404563484.json]
2025-11-13 11:25:02.0191 IST [Bridge CLI] INFO: network.airgap = false [blackducksca_input8761691229404563484.json]
2025-11-13 11:25:02.0192 IST [Bridge CLI] INFO: ------------------------------------------------------------
2025-11-13 11:25:02.0192 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca
2025-11-13 11:25:02.0195 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Controller
2025-11-13 11:25:02.0262 IST [Bridge CLI] INFO: Starting Adapter: Check pull request
2025-11-13 11:25:02.0742 IST [Check pull request] INFO: Provided value for resource 'environment.scan.pull'
2025-11-13 11:25:02.0745 IST [Check pull request] INFO: Adapter finished
2025-11-13 11:25:02.5210 IST [Blackduck SCA Controller] INFO: Found Black Duck SCA Detect jar file "detect-11.0.0.jar" in "/Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0"
2025-11-13 11:25:02.5362 IST [Blackduck SCA Controller] INFO: Provided value for resource 'detect.execution.path'
2025-11-13 11:25:02.5363 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-detect
2025-11-13 11:25:02.5363 IST [Bridge CLI] INFO: Starting adapters for stage scm
2025-11-13 11:25:02.5363 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-post-processing
2025-11-13 11:25:02.5384 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Results
2025-11-13 11:25:02.5384 IST [Bridge CLI] INFO: Starting Adapter: SCM Checker
2025-11-13 11:25:02.5384 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Detect Execution
2025-11-13 11:25:02.5384 IST [Bridge CLI] INFO: Starting Adapter: Detect Component Locator
2025-11-13 11:25:02.5426 IST [Blackduck SCA Controller] INFO: Adapter finished
2025-11-13 11:25:02.6267 IST [Blackduck SCA Detect Execution] INFO: Running command /Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home/bin/java -jar /Users/madhusud/.blackduck/bridge/tools/blackduck-detect/11.0.0/detect-11.0.0.jar --detect.cleanup=false --detect.bdio.file.name=scan --detect.bdio.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact --detect.output.path=/Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect --blackduck.offline.mode=false --blackduck.url=https://saastest.app.blackduck.com --blackduck.api.token= --detect.wait.for.results=true --detect.blackduck.scan.mode=INTELLIGENT
2025-11-13 11:25:03.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect-Self-Updater:  Checking https://saastest.app.blackduck.com/api/tools/detect API for centrally managed Detect version to download to /Users/madhusud/tmp.
2025-11-13 11:25:04.0000 IST [Blackduck SCA Detect Execution][main] WARNING: --- Detect-Self-Updater:  Unable to download jar from https://saastest.app.blackduck.com/api/tools/detect.
2025-11-13 11:25:04.0000 IST [Blackduck SCA Detect Execution][main] WARNING: --- Detect-Self-Updater:  Response code from https://saastest.app.blackduck.com/api/tools/detect was: 403 Forbidden
2025-11-13 11:25:05.2047 IST [Blackduck SCA Detect Execution] INFO: ______     _            _
2025-11-13 11:25:05.2048 IST [Blackduck SCA Detect Execution] INFO: |  _  \   | |          | |
2025-11-13 11:25:05.2048 IST [Blackduck SCA Detect Execution] INFO: | | | |___| |_ ___  ___| |_
2025-11-13 11:25:05.2048 IST [Blackduck SCA Detect Execution] INFO: | | | / _ \ __/ _ \/ __| __|
2025-11-13 11:25:05.2048 IST [Blackduck SCA Detect Execution] INFO: | |/ /  __/ ||  __/ (__| |_
2025-11-13 11:25:05.2048 IST [Blackduck SCA Detect Execution] INFO: |___/ \___|\__\___|\___|\__|
2025-11-13 11:25:05.2049 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-13 11:25:05.2909 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-13 11:25:05.2910 IST [Blackduck SCA Detect Execution] INFO: Detect Version: 11.0.0
2025-11-13 11:25:05.2910 IST [Blackduck SCA Detect Execution] INFO: 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Current property values:
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- --property = value [notes]
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ------------------------------------------------------------
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.api.token = **************************************************************************************************** [cmd] 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.offline.mode = false [cmd] 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- blackduck.url = https://saastest.app.blackduck.com [cmd] 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.bdio.file.name = scan [cmd] 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.bdio.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/bdio/blackduck_artifact [cmd] 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.blackduck.scan.mode = INTELLIGENT [cmd] 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.cleanup = false [cmd] 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.excluded.directories = /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main/nodejs-npm/.bridge [env] 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.output.path = /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect [cmd] 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.project.name = MBP_Github_Polaris_Build_Scan [env] 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- detect.wait.for.results = true [cmd] 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ------------------------------------------------------------
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect build date: 2025-10-30
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Source directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main/nodejs-npm
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Output directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Run directory: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-13-05-55-05-283
2025-11-13 11:25:05.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] ERROR: --- The connection was not successful for an unknown reason. If an api token is being used, it could be incorrect.
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] ERROR: --- Failed to connect to the Black Duck SCA server
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Creating status file: /Users/madhusud/Jenkins_Testing/Nodes/workspace/P_Github_Polaris_Build_Scan_main/nodejs-npm/.bridge/blackduck_sca_detect_execution/detect/runs/2025-11-13-05-55-05-283/status/status.json
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Skipping cleanup, it is disabled.
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======== Detect Issues ========
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- EXCEPTIONS:
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 	Detect Boot Error
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 		Could not communicate with Black Duck: The connection was not successful for an unknown reason. If an api token is being used, it could be incorrect.
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ======== Detect Status ========
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] ERROR: --- Overall Status: FAILURE_BLACKDUCK_CONNECTIVITY - Detect was unable to connect to Black Duck SCA. Check your configuration and connection.
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- ===============================
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- 
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] INFO: --- Detect duration: 00h 00m 03s 766ms
2025-11-13 11:25:06.0000 IST [Blackduck SCA Detect Execution][main] ERROR: --- Exiting with code 1 - FAILURE_BLACKDUCK_CONNECTIVITY
2025-11-13 11:25:06.9579 IST [Blackduck SCA Detect Execution] ERROR: exit status 1
2025-11-13 11:25:06.9649 IST [Blackduck SCA Detect Execution] INFO: Provided value for resource 'detect.results.path'
2025-11-13 11:25:06.9651 IST [Blackduck SCA Detect Execution] ERROR: Adapter failed: exit status 1
2025-11-13 11:25:07.0178 IST [Blackduck SCA Results] INFO: Skipping Blackduck SCA issues retrieval as "blackducksca.fixpr.enabled" is configured to false
2025-11-13 11:25:07.0233 IST [Blackduck SCA Results] INFO: Adapter finished
2025-11-13 11:25:07.0838 IST [SCM Checker] INFO: Provided value for resource 'jenkins.enabled'
2025-11-13 11:25:07.0839 IST [Bridge CLI] INFO: Starting adapters for stage blackducksca-policy-violations-fetcher
2025-11-13 11:25:07.0843 IST [Bridge CLI] INFO: Starting Adapter: Blackduck SCA Policy Violations Fetcher
2025-11-13 11:25:07.0844 IST [SCM Checker] INFO: Adapter finished
2025-11-13 11:25:07.1205 IST [Detect Component Locator] INFO: skipping fix pull requests creation as "blackducksca.fixpr.enabled" is configured to false
2025-11-13 11:25:07.1254 IST [Detect Component Locator] INFO: Adapter finished
2025-11-13 11:25:07.1669 IST [Blackduck SCA Policy Violations Fetcher] ERROR: There is no detect scan to gather results from
2025-11-13 11:25:07.1718 IST [Blackduck SCA Policy Violations Fetcher] INFO: Provided value for resource 'blackducksca.projectBomUrl'
2025-11-13 11:25:07.1720 IST [Blackduck SCA Policy Violations Fetcher] INFO: Adapter finished
******************************* END EXECUTION OF BRIDGE CLI *******************************
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
Configuration: [githubOrg:blackducksca-jenkins-samples, repoName:full-scan, credentialsId:github-pat-logs-publisher, maxRetries:3, retentionCount:5, jobNamePrefixes:[MBP_Github_, MBP_, Github_, Pipeline_, Job_, Build_]]
[Pipeline] echo
Job Name: MBP_Github_Polaris_Build_Scan/main
[Pipeline] echo
Build Number: 1
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