---
id: version-0.41-testing
title: testing
original_id: testing
---
<a id="content"></a><h1><a class="anchor" name="testing"></a>Testing <a class="hash-link" href="docs/testing.html#testing">#</a></h1><div><h2><a class="anchor" name="running-tests-and-contributing"></a>Running Tests and Contributing <a class="hash-link" href="docs/testing.html#running-tests-and-contributing">#</a></h2><p>This document is about running tests on React Native itself. If you're interested in testing a React Native app, check out the <a href="http://facebook.github.io/jest/docs/tutorial-react-native.html" target="_blank">React Native Tutorial</a> on the Jest website.</p><p>The React Native repo has several tests you can run to verify you haven't caused a regression with your PR.  These tests are run with the <a href="http://docs.travis-ci.com/" target="_blank">Travis</a> and <a href="https://circleci.com/" target="_blank">CircleCI</a> continuous integration systems, which will automatically annotate pull requests with the test results.</p><p>Whenever you are fixing a bug or adding new functionality to React Native, you should add a test that covers it. Depending on the change you're making, there are different types of tests that may be appropriate.</p><h2><a class="anchor" name="jest-tests"></a>Jest Tests <a class="hash-link" href="docs/testing.html#jest-tests">#</a></h2><p>Jest tests are JavaScript-only tests run on the command line with node. You can run the existing React Native jest tests with:</p><div class="prism language-javascript">$ cd react<span class="token operator">-</span>native
$ npm test</div><p>It's a good idea to add a Jest test when you are working on a change that only modifies JavaScript code.</p><p>The tests themselves live in the <code>__tests__</code> directories of the files they test.  See <a href="https://github.com/facebook/react-native/blob/master/Libraries/Components/Touchable/__tests__/TouchableHighlight-test.js" target="_blank"><code>TouchableHighlight-test.js</code></a> for a basic example.</p><h2><a class="anchor" name="android-unit-tests"></a>Android Unit Tests <a class="hash-link" href="docs/testing.html#android-unit-tests">#</a></h2><p>The Android unit tests do not run in an emulator. They just use a normal Java installation. You do need to install Java 8. In particular, the default OS X Java install is insufficient.</p><p>You also need to install the <a href="https://buckbuild.com/setup/install.html" target="_blank">Buck build tool</a>.</p><p>To run the Android unit tests:</p><div class="prism language-javascript">$ cd react<span class="token operator">-</span>native
$ <span class="token punctuation">.</span><span class="token operator">/</span>scripts<span class="token operator">/</span>run<span class="token operator">-</span>android<span class="token operator">-</span>local<span class="token operator">-</span>unit<span class="token operator">-</span>tests<span class="token punctuation">.</span>sh</div><p>It's a good idea to add an Android unit test whenever you are working on code that can be tested by Java code alone. The Android unit tests live under <a href="https://github.com/facebook/react-native/tree/master/ReactAndroid/src/test/java/com/facebook/react" target="_blank"><code>ReactAndroid/src/tests</code></a>, so you can browse through that directory for good examples of tests.</p><h2><a class="anchor" name="android-integration-tests"></a>Android Integration Tests <a class="hash-link" href="docs/testing.html#android-integration-tests">#</a></h2><p>To run the integration tests, you need to install the Android NDK. See <a href="/react-native/docs/android-building-from-source.html#prerequisites" target="">Prerequisites</a>.</p><p>You also need to install the <a href="https://buckbuild.com/setup/install.html" target="_blank">Buck build tool</a>.</p><p>We recommend running the Android integration tests in an emulator, although you can also use a real Android device. It's a good idea to keep the emulator running with a visible window. That way if your tests stall, you can look at the emulator to debug.</p><p>Some devices and some emulator configurations may not work with the tests. We do maintain an emulator configuration that works, as the standard for testing. To run this emulator config:</p><div class="prism language-javascript">$ cd react<span class="token operator">-</span>native
$ <span class="token punctuation">.</span><span class="token operator">/</span>scripts<span class="token operator">/</span>run<span class="token operator">-</span>android<span class="token operator">-</span>emulator<span class="token punctuation">.</span>sh</div><p>Once you have an emulator running, to run the integration tests:</p><div class="prism language-javascript">$ cd react<span class="token operator">-</span>native
$ <span class="token punctuation">.</span><span class="token operator">/</span>scripts<span class="token operator">/</span>run<span class="token operator">-</span>android<span class="token operator">-</span>local<span class="token operator">-</span>integration<span class="token operator">-</span>tests<span class="token punctuation">.</span>sh</div><p>The integration tests should only take a few minutes to run on a modern developer machine.</p><p>It's a good idea to add an Android integration test whenever you are working on code that needs both JavaScript and Java to be tested in conjunction. The Android integration tests live under <a href="https://github.com/facebook/react-native/tree/master/ReactAndroid/src/androidTest/java/com/facebook/react/tests" target="_blank"><code>ReactAndroid/src/androidTest</code></a>, so you can browse through that directory for good examples of tests. </p><h2><a class="anchor" name="ios-integration-tests"></a>iOS Integration Tests <a class="hash-link" href="docs/testing.html#ios-integration-tests">#</a></h2><p>React Native provides facilities to make it easier to test integrated components that require both native and JS components to communicate across the bridge.  The two main components are <code>RCTTestRunner</code> and <code>RCTTestModule</code>.  <code>RCTTestRunner</code> sets up the ReactNative environment and provides facilities to run the tests as <code>XCTestCase</code>s in Xcode (<code>runTest:module</code> is the simplest method).  <code>RCTTestModule</code> is exported to JS as <code>NativeModules.TestModule</code>.  The tests themselves are written in JS, and must call <code>TestModule.markTestCompleted()</code> when they are done, otherwise the test will timeout and fail.  Test failures are primarily indicated by throwing a JS exception.  It is also possible to test error conditions with <code>runTest:module:initialProps:expectErrorRegex:</code> or <code>runTest:module:initialProps:expectErrorBlock:</code> which will expect an error to be thrown and verify the error matches the provided criteria.  See <a href="https://github.com/facebook/react-native/blob/master/IntegrationTests/IntegrationTestHarnessTest.js" target="_blank"><code>IntegrationTestHarnessTest.js</code></a>, <a href="https://github.com/facebook/react-native/blob/master/Examples/UIExplorer/UIExplorerIntegrationTests/UIExplorerIntegrationTests.m" target="_blank"><code>UIExplorerIntegrationTests.m</code></a>, and <a href="https://github.com/facebook/react-native/blob/master/IntegrationTests/IntegrationTestsApp.js" target="_blank">IntegrationTestsApp.js</a> for example usage and integration points.</p><p>You can run integration tests locally with cmd+U in the IntegrationTest and UIExplorer apps in Xcode.</p><h2><a class="anchor" name="ios-screenshot-snapshot-tests"></a>iOS Screenshot/Snapshot Tests <a class="hash-link" href="docs/testing.html#ios-screenshot-snapshot-tests">#</a></h2><p>A common type of integration test is the snapshot test.  These tests render a component, and verify snapshots of the screen against reference images using <code>TestModule.verifySnapshot()</code>, using the <a href="https://github.com/facebook/ios-snapshot-test-case" target="_blank"><code>FBSnapshotTestCase</code></a> library behind the scenes.  Reference images are recorded by setting <code>recordMode = YES</code> on the <code>RCTTestRunner</code>, then running the tests.  Snapshots will differ slightly between 32 and 64 bit, and various OS versions, so it's recommended that you enforce tests are run with the correct configuration.  It's also highly recommended that all network data be mocked out, along with other potentially troublesome dependencies.  See <a href="https://github.com/facebook/react-native/blob/master/IntegrationTests/SimpleSnapshotTest.js" target="_blank"><code>SimpleSnapshotTest</code></a> for a basic example.</p><p>If you make a change that affects a snapshot test in a PR, such as adding a new example case to one of the examples that is snapshotted, you'll need to re-record the snapshot reference image.  To do this, simply change to <code>_runner.recordMode = YES;</code> in <a href="https://github.com/facebook/react-native/blob/master/Examples/UIExplorer/UIExplorerIntegrationTests/UIExplorerSnapshotTests.m#L42" target="_blank">UIExplorer/UIExplorerSnapshotTests.m</a>, re-run the failing tests, then flip record back to <code>NO</code> and submit/update your PR and wait to see if the Travis build passes.</p></div><div class="docs-prevnext"><a class="docs-prev" href="docs/debugging.html#content">← Prev</a><a class="docs-next" href="docs/running-on-device.html#content">Next →</a></div><p class="edit-page-block">You can <a target="_blank" href="https://github.com/facebook/react-native/blob/master/docs/Testing.md">edit the content above on GitHub</a> and send us a pull request!</p>