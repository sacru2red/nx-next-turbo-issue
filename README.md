# message

```
$ nx dev org

> nx run org:dev

  ▲ Next.js 14.2.16 (turbo)
  - Local:        http://localhost:3001
 ✓ Starting...
 ✓ Ready in 2.3s
 ○ Compiling / ...
 ⨯ ./node_modules/nx/src/tasks-runner
Module not found: Can't resolve '/ROOT/node_modules/nx/src/tasks-runner/batch/run-batch.js'
server relative imports are not implemented yet. Please try an import relative to the file you are importing from.
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/tasks-runner
Module not found: Can't resolve '/ROOT/node_modules/nx/src/tasks-runner/remove-old-cache-records.js'
server relative imports are not implemented yet. Please try an import relative to the file you are importing from.
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/@nx/devkit/src/utils/convert-nx-executor.js:51:12
Module not found: Can't resolve '@angular-devkit/architect'
  49 |         return toObservable(promise());
  50 |     };
> 51 |     return require('@angular-devkit/architect').createBuilder(builderFunction);
     |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  52 | }
  53 | function toObservable(promiseOrAsyncIterator) {
  54 |     return new (require('rxjs').Observable)((subscriber) => {
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/adapter/ngcli-adapter.js:45:27
Module not found: Can't resolve '@angular-devkit/architect'
  43 |         return [];
  44 |     });
> 45 |     const { Architect } = require('@angular-devkit/architect');
     |                           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  46 |     const architect = new Architect(architectHost, registry);
  47 |     const { firstValueFrom } = require('rxjs');
  48 |     const toPromise = (obs) => firstValueFrom ? firstValueFrom(obs) : obs.toPromise();
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/adapter/ngcli-adapter.js:115:27
Module not found: Can't resolve '@angular-devkit/architect'
  113 | }
  114 | async function scheduleTarget(root, opts, verbose) {
> 115 |     const { Architect } = require('@angular-devkit/architect');
      |                           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  116 |     const logger = (0, exports.getLogger)(verbose);
  117 |     const fsHost = new NxScopedHostForBuilders(root);
  118 |     const { workspace } = await core_1.workspaces.readWorkspace('angular.json', core_1.workspaces.createWorkspaceHost(fsHost));
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/adapter/ngcli-adapter.js:782:129
Module not found: Can't resolve '@angular-devkit/architect/node'
  780 | }
  781 | async function getWrappedWorkspaceNodeModulesArchitectHost(workspace, root, projects) {
> 782 |     const { WorkspaceNodeModulesArchitectHost: AngularWorkspaceNodeModulesArchitectHost, } = await Promise.resolve().then(() => require('@angular-devkit/architect/node'));
      |                                                                                                                                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  783 |     class WrappedWorkspaceNodeModulesArchitectHost extends AngularWorkspaceNodeModulesArchitectHost {
  784 |         constructor(workspace, root, projects) {
  785 |             super(workspace, root);
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/adapter/ngcli-adapter.js:11:16
Module not found: Can't resolve '@angular-devkit/core'
   9 | exports.mockSchematicsForTesting = mockSchematicsForTesting;
  10 | exports.wrapAngularDevkitSchematic = wrapAngularDevkitSchematic;
> 11 | const core_1 = require("@angular-devkit/core");
     |                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  12 | const node_1 = require("@angular-devkit/core/node");
  13 | const chalk = require("chalk");
  14 | const path_1 = require("path");
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/adapter/ngcli-adapter.js:36:28
Module not found: Can't resolve '@angular-devkit/core'
  34 |     // the top level import is not patched because it is imported before the
  35 |     // patching happens so we require it here to use the patched version below
> 36 |     const { workspaces } = require('@angular-devkit/core');
     |                            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  37 |     const { workspace } = await workspaces.readWorkspace('angular.json', workspaces.createWorkspaceHost(fsHost));
  38 |     const architectHost = await getWrappedWorkspaceNodeModulesArchitectHost(workspace, context.root, context.projectsConfigurations.projects);
  39 |     const registry = new core_1.schema.CoreSchemaRegistry();
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/adapter/ngcli-adapter.js:12:16
Module not found: Can't resolve '@angular-devkit/core/node'
  10 | exports.wrapAngularDevkitSchematic = wrapAngularDevkitSchematic;
  11 | const core_1 = require("@angular-devkit/core");
> 12 | const node_1 = require("@angular-devkit/core/node");
     |                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  13 | const chalk = require("chalk");
  14 | const path_1 = require("path");
  15 | const rxjs_1 = require("rxjs");
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/adapter/ngcli-adapter.js:176:56
Module not found: Can't resolve '@angular-devkit/schematics'
  174 |         packageManager: (0, package_manager_1.detectPackageManager)(),
  175 |         root: (0, core_1.normalize)(root),
> 176 |         registry: new core_1.schema.CoreSchemaRegistry(require('@angular-devkit/schematics').formats.standardFormats),
      |                                                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  177 |         resolvePaths: [process.cwd(), root],
  178 |         engineHostCreator: (options) => createNodeModulesEngineHost(options.resolvePaths, projects),
  179 |     });
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/adapter/ngcli-adapter.js:170:26
Module not found: Can't resolve '@angular-devkit/schematics/tools'
  168 | }
  169 | function createWorkflow(fsHost, root, opts, projects) {
> 170 |     const NodeWorkflow = require('@angular-devkit/schematics/tools').NodeWorkflow;
      |                          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  171 |     const workflow = new NodeWorkflow(fsHost, {
  172 |         force: false,
  173 |         dryRun: opts.dryRun,
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/adapter/ngcli-adapter.js:139:35
Module not found: Can't resolve '@angular-devkit/schematics/tools'
  137 | }
  138 | function createNodeModulesEngineHost(resolvePaths, projects) {
> 139 |     const NodeModulesEngineHost = require('@angular-devkit/schematics/tools')
      |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  140 |         .NodeModulesEngineHost;
  141 |     class NxNodeModulesEngineHost extends NodeModulesEngineHost {
  142 |         constructor() {
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/adapter/ngcli-adapter.js:181:50
Module not found: Can't resolve '@angular-devkit/schematics/tools'
  179 |     });
  180 |     workflow.registry.addPostTransform(core_1.schema.transforms.addUndefinedDefaults);
> 181 |     workflow.engineHost.registerOptionsTransform(require('@angular-devkit/schematics/tools').validateOptionsWithSchema(workflow.registry));
      |                                                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  182 |     if (opts.interactive) {
  183 |         workflow.registry.usePromptProvider(createPromptProvider());
  184 |     }
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/utils/powerpack.js:18:126
Module not found: Can't resolve '@nx/powerpack-license'
  16 | async function getPowerpackLicenseInformation() {
  17 |     try {
> 18 |         const { getPowerpackLicenseInformation, getPowerpackLicenseInformationAsync, } = (await Promise.resolve().then(() => require('@nx/powerpack-license')));
     |                                                                                                                              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  19 |         return (getPowerpackLicenseInformationAsync ?? getPowerpackLicenseInformation)(workspace_root_1.workspaceRoot);
  20 |     }
  21 |     catch (e) {
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/@swc/core/index.js:68:28
Module not found: Can't resolve '@swc/wasm'
  66 |     catch (_) {
  67 |         // postinstall supposed to install `@swc/wasm` already
> 68 |         fallbackBindings = require("@swc/wasm");
     |                            ^^^^^^^^^^^^^^^^^^^^
  69 |     }
  70 |     finally {
  71 |         return binding;
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/tsconfig-paths/lib/filesystem.js:31:12
Module not found
  29 |     }
  30 |     // eslint-disable-next-line @typescript-eslint/no-require-imports
> 31 |     return require(packageJsonPath);
     |            ^^^^^^^^^^^^^^^^^^^^^^^^
  32 | }
  33 | exports.readJsonFromDiskSync = readJsonFromDiskSync;
  34 | function readJsonFromDiskAsync(path,
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/@nx/devkit/src/utils/package-json.js:372:12
Module not found
  370 | }
  371 | function getPackageVersion(pkg) {
> 372 |     return require((0, path_1.join)(pkg, 'package.json')).version;
      |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  373 | }
  374 | /**
  375 |  * @description The version of Nx used by the workspace. Returns null if no version is found.
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/prettier/third-party.js:83:34
Module not found
  81 |       delete require.cache[filePath];
  82 |       const parent = require.cache[parentPath];
> 83 |       return parent === void 0 ? require(filePath) : parent.require(filePath);
     |                                  ^^^^^^^^^^^^^^^^^
  84 |     };
  85 |   }
  86 | });
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/nx-cloud/update-manager.js:61:32
Module not found
  59 |             return {
  60 |                 version: currentBundle.version,
> 61 |                 nxCloudClient: require(currentBundle.fullPath),
     |                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  62 |             };
  63 |         }
  64 |         const { version, url } = verifyBundleResponse.data;
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/nx-cloud/update-manager.js:47:35
Module not found
  45 |                 throw new NxCloudEnterpriseOutdatedError(options.url);
  46 |             }
> 47 |             const nxCloudClient = require(currentBundle.fullPath);
     |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  48 |             if (nxCloudClient.commands === undefined) {
  49 |                 throw new NxCloudEnterpriseOutdatedError(options.url);
  50 |             }
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/command-line/run/executor-utils.js:71:31
Module not found
  69 |     }
  70 |     const basePath = (0, path_1.dirname)(packageJsonPath);
> 71 |     const executorsFilePath = require.resolve((0, path_1.join)(basePath, executorsFile));
     |                               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  72 |     const executorsJson = (0, fileutils_1.readJsonFile)(executorsFilePath);
  73 |     const executorConfig = executorsJson.executors?.[executor] || executorsJson.builders?.[executor];
  74 |     if (!executorConfig) {
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/prettier/index.js:38143:10
Module not found
  38141 |       const externalPlugins = [...uniqByKey([...externalManualLoadPluginInfos, ...externalAutoLoadPluginInfos], "requirePath").map((externalPluginInfo) => Object.assign({
  38142 |         name: externalPluginInfo.name
> 38143 |       }, require(externalPluginInfo.requirePath))), ...externalPluginInstances];
        |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  38144 |       return [...internalPlugins, ...externalPlugins];
  38145 |     }
  38146 |     function findPluginsInNodeModules(nodeModulesDir) {
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/ts-node/dist/transpilers/swc.js:29:23
Module not found
  27 |             }
  28 |         }
> 29 |         swcInstance = require(swcResolved);
     |                       ^^^^^^^^^^^^^^^^^^^^
  30 |     }
  31 |     else {
  32 |         swcInstance = swc;
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/command-line/generate/generator-utils.js:56:30
Module not found
  54 |             throw new Error(`The "${collectionName}" package does not support Nx generators.`);
  55 |         }
> 56 |         generatorsFilePath = require.resolve((0, path_1.join)((0, path_1.dirname)(packageJsonPath), generatorsFile));
     |                              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  57 |     }
  58 |     const generatorsJson = (0, fileutils_1.readJsonFile)(generatorsFilePath);
  59 |     let normalizedGeneratorName = findFullGeneratorName(generator, generatorsJson.generators) ||
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/config/schema-utils.js:22:24
Module not found
  20 |             (0, plugins_1.registerPluginTSTranspiler)();
  21 |         }
> 22 |         const module = require(modulePath);
     |                        ^^^^^^^^^^^^^^^^^^^
  23 |         return implementationExportName
  24 |             ? module[implementationExportName]
  25 |             : module.default ?? module;
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/prettier/index.js:18428:31
Module not found
  18426 |                 paths: [dir]
  18427 |               });
> 18428 |               result.config = require(modulePath);
        |                               ^^^^^^^^^^^^^^^^^^^
  18429 |             }
  18430 |             if (typeof result.config !== "object") {
  18431 |               throw new TypeError(`Config is only allowed to be an object, but received ${typeof result.config} in "${result.filepath}"`);
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/adapter/ngcli-adapter.js:158:38
Module not found
  156 |                     throw new Error(`The "${name}" package does not support Nx generators or Angular Devkit schematics.`);
  157 |                 }
> 158 |                 collectionFilePath = require.resolve((0, path_1.join)((0, path_1.dirname)(packageJsonPath), schematics ?? generators));
      |                                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  159 |             }
  160 |             return collectionFilePath;
  161 |         }
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/nx-cloud/update-manager.js:71:31
Module not found
  69 |         const fullPath = await downloadAndExtractClientBundle(axios, runnerBundleInstallDirectory, version, url);
  70 |         (0, debug_logger_1.debugLog)('Done: ', fullPath);
> 71 |         const nxCloudClient = require(fullPath);
     |                               ^^^^^^^^^^^^^^^^^
  72 |         if (nxCloudClient.commands === undefined) {
  73 |             throw new NxCloudEnterpriseOutdatedError(options.url);
  74 |         }
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/adapter/ngcli-adapter.js:590:26
Module not found
  588 |     }
  589 |     if ((0, path_1.extname)(name)) {
> 590 |         collectionPath = require.resolve(name);
      |                          ^^^^^^^^^^^^^^^^^^^^^
  591 |     }
  592 |     else {
  593 |         const { path: packageJsonPath, packageJson } = (0, package_json_1.readModulePackageJson)(name, (0, installation_directory_1.getNxRequirePaths)(process.cwd()));
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/ts-node/dist-raw/node-internal-modules-cjs-helpers.js:67:21
Module not found
  65 |       get: () => {
  66 |         // Node 12 hack; remove when we drop node12 support
> 67 |         const lib = (dummyModule.require || require)(name);
     |                     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  68 |
  69 |         // Disable the current getter/setter and set up a new
  70 |         // non-enumerable property.
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/ts-node/dist/transpilers/swc.js:12:23
Module not found
  10 |     if (typeof swc === 'string') {
  11 |         swcDepName = swc;
> 12 |         swcInstance = require(transpilerConfigLocalResolveHelper(swc, true));
     |                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  13 |     }
  14 |     else if (swc == null) {
  15 |         let swcResolved;
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/nx-cloud/utilities/axios.js:16:40
Module not found
  14 |     }
  15 |     if (options.customProxyConfigPath) {
> 16 |         const { nxCloudProxyConfig } = require((0, path_1.join)(process.cwd(), options.customProxyConfigPath));
     |                                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  17 |         axiosConfigBuilder = nxCloudProxyConfig ?? axiosConfigBuilder;
  18 |     }
  19 |     return require('axios').create(axiosConfigBuilder({
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/nx-cloud/update-manager.js:83:24
Module not found
  81 |     return {
  82 |         version: currentBundle.version,
> 83 |         nxCloudClient: require(currentBundle.fullPath),
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  84 |     };
  85 | }
  86 | const runnerBundleInstallDirectory = (0, path_1.join)(cache_directory_1.cacheDir, 'cloud');
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/tasks-runner/cache.js:170:94
Module not found
  168 |         let getRemoteCache = null;
  169 |         try {
> 170 |             getRemoteCache = (await Promise.resolve(`${this.resolvePackage(pkg)}`).then(s => require(s))).getRemoteCache;
      |                                                                                              ^^^^^^^^^^
  171 |         }
  172 |         catch {
  173 |             return null;
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/project-graph/plugins/load-resolved-plugin.js:11:64
Module not found
   9 | }
  10 | async function importPluginModule(pluginPath) {
> 11 |     const m = await Promise.resolve(`${pluginPath}`).then(s => require(s));
     |                                                                ^^^^^^^^^^
  12 |     if (m.default &&
  13 |         ('createNodes' in m.default ||
  14 |             'createNodesV2' in m.default ||
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/adapter/ngcli-adapter.js:811:39
Module not found
  809 |             }
  810 |             const basePath = (0, path_1.dirname)(packageJsonPath);
> 811 |             const executorsFilePath = require.resolve((0, path_1.join)(basePath, executorsFile));
      |                                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  812 |             const executorsJson = (0, fileutils_1.readJsonFile)(executorsFilePath);
  813 |             const executorConfig = executorsJson.builders?.[builder] ?? executorsJson.executors?.[builder];
  814 |             if (!executorConfig) {
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/nx/src/native/index.js:69:28
Module not found
  67 |     localNodeFiles.some((f) => modulePath.endsWith(f))
  68 |   ) {
> 69 |     const nativeLocation = require.resolve(modulePath);
     |                            ^^^^^^^^^^^^^^^^^^^^^^^^^^^
  70 |     const fileName = basename(nativeLocation);
  71 |
  72 |     // we copy the file to a workspace-scoped tmp directory and prefix with nxVersion to avoid stale files being loaded
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/ts-node/dist/index.js:247:39
Module not found
  245 |                 : projectLocalResolveHelper;
  246 |             const transpilerPath = transpilerConfigLocalResolveHelper(transpilerName, true);
> 247 |             const transpilerFactory = require(transpilerPath)
      |                                       ^^^^^^^^^^^^^^^^^^^^^^^
  248 |                 .create;
  249 |             return createTranspiler;
  250 |             function createTranspiler(compilerOptions, nodeModuleEmitKind) {
https://nextjs.org/docs/messages/module-not-found
 ⨯ ./node_modules/yargs-parser/build/index.cjs:1029:20
Module not found
  1027 |     require: (path) => {
  1028 |         if (typeof require !== 'undefined') {
> 1029 |             return require(path);
       |                    ^^^^^^^^^^^^^
  1030 |         }
  1031 |         else if (path.match(/\.json$/)) {
  1032 |             return JSON.parse(fs.readFileSync(path, 'utf8'));
https://nextjs.org/docs/messages/module-not-found
```
