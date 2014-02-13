Crosswalk-Tizen-sync-Tool
=========================

###Introduction###

Crosswalk-Tizen-sync-Tool allow the user to locally catch the latest Crosswalk development release as explain in
https://crosswalk-project.org/#contribute/building_crosswalk in a scope of building for the Tizen environment.

###Usage example###

To use this script:
```bash
git clone git@github.com:eurogiciel-oss/Crosswalk-Tizen-sync-Tool.git
cd Crosswalk-Tizen-sync-Tool
./Tizen_sync
```

###Results###

- After launching the script, you should have the following directories populated with latest Crosswalk development release:

```
.
├── 32.0.1700.102
├── depot_tools
├── README.md
├── src
├── Tizen_Crosswalk
└── Tizen_sync
```

- Here is an example commands lines of how to build Crosswalk rpm for Tizen:

```bash
cd src/xwalk
gbs build --include-all -A x86_64 -P generic-x86_64 --define 'BUILDDIR_NAME /var/tmp/xwalk-build' -C
```

- Also, following forked projects are a new git remote "eurogiciel" to ease developpers to perform upstream's pull-request procedure:

| Path                   | Remote     | URL                                                  |
| ---------------------- | ---------- | ---------------------------------------------------- | 
| src/third_party/WebKit | eurogiciel | git@github.com:eurogiciel-oss/blink-crosswalk.git    |
| src/xwalk              | eurogiciel | git@github.com:eurogiciel-oss/crosswalk.git          |
| src                    | eurogiciel | git@github.com:eurogiciel-oss/chromium-crosswalk.git |


