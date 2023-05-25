
[Blog Codemagic](https://blog.codemagic.io/flutter-monorepos/)

Structure Folder
   
  ```
  example_monorepo/
    apps/
      counter_app
    packages/
      ...
    melos.yaml
    pubspec.yaml
  ```

* Step 1
  create flutter project
 
* Step 2 
  - install Melos , following command in your terminal:
    `dart pub global activate melos `
  - add Melos as a development dependency by running the following command:
    `dart pub add melos --dev `
  - create file  `melos.yaml`
  - add script in your  `melos.yaml` to configure the workspace 
  ```
   name: <your-project-name>

   # A list of paths to local packages that are included in the Melos workspace.
   # Each entry can be a specific path or a glob pattern.
   packages:
   - "apps/*"
   - "packages/**"
   # This enables a new mechanism for linking local packages, which integrates
   # better with other tooling (e.g. dart tool, flutter tool, IDE plugins) than the
   # mechanism currently being used by default. Please read the documentation for
   # usePubspecOverrides before enabling this feature.   
  ```
   [Melos Documentation](https://melos.invertase.dev/getting-started#setup)
  
    [Migration From version 3.0.0](https://melos.invertase.dev/guides/migrations#200-to-300)
  - add script in your `pubspec.yaml` to ensure everyone working in the workspace
    (as well as CI jobs) is using the same version of Melos
   ```
  name: <your-project-name>

  environment:
  sdk: ">=2.18.0 <3.0.0"
  ```
  
  - run the bootstrap command to initialize Melos , following command in your terminal:
     `melos bootstrap`.

  
