
[Article](https://blog.codemagic.io/flutter-monorepos/)

Structure Folder
 ```example_monorepo/
  apps/
    counter_app
  packages/
    ...
  melos.yaml
  pubspec.yaml```

* Step 1
  create flutter project
 
* Step 2 
  - install Melos , following command in your terminal:
    `dart pub global activate melos`
  - add Melos as a development dependency by running the following command:
    `dart pub add melos --dev`
  - create file `melos.yaml`
  - add script in your `melos.yaml` to configure the workspace 
    [Migration From version 3.0.0](https://melos.invertase.dev/guides/migrations#200-to-300)
  - add script in your `pubspec.yaml` to ensure everyone working in the workspace
    (as well as CI jobs) is using the same version of Melos
  - run the bootstrap command to initialize Melos , following command in your terminal:
    `melos bootstrap`.

  