Rules for external python packages in bazel.

See ```WORKSPACE``` for defining external libraries

See ```demo/third_party/BUILD``` for defining python libraries based on them

See ```demo/src/app.py``` for imports that hack sys.path for loading external
libraries.

See ```demo/src/bundle_app.py``` for loading multiple external deps using
a single rule.

Future plans:
* virtualenv_bin and virtualenv_test targets. Easy to use, depending only on
  pip
* Speak with bazel devs for md5 support in new_http_archive
* Speak with bazel devs for getting eggs into runfiles

Limitations:
* The build is reproductible but is not portable, as the loader libs
wil work with local absolute paths.
