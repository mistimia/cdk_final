# cdk_final
Running cdk with codecommit construct projen


Projen.js

const { AwsCdkConstructLibrary, NodePackageManager } = require('projen');
const project = new AwsCdkConstructLibrary({
  author: 'ishita',
  authorAddress: 'ishitasaxena78@yahoo.in',
  cdkVersion: '1.95.2',
  defaultReleaseBranch: 'main',
  name: 'v5',
  repositoryUrl: 'https://github.com/ishitasaxena78/v5.git',
  cdkDependencies: ['@aws-cdk/core', '@aws-cdk/aws-s3'],
  packageManager: NodePackageManager.NPM,
  docgen: true,
  eslint: true,
  // cdkDependencies: undefined,      /* Which AWS CDK modules (those that start with "@aws-cdk/") does this library require when consumed? */
  // cdkTestDependencies: undefined,  /* AWS CDK modules required for testing. */
  // deps: [],                        /* Runtime dependencies of this module. */
  // description: undefined,          /* The description is just a string that helps people understand the purpose of the package. */
  // devDeps: [],                     /* Build dependencies for this module. */
  // packageName: undefined,          /* The "name" in package.json. */
  // release: undefined,              /* Add release management to this project. */
});
project.synth();
