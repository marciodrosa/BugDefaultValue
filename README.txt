Memo project with steps to reproduce an issue.

Steps:
1) Open the project in the editor
2) Open MyMap
3) World Outliner > select MyActor

There are 3 actor components:
- MyComponent: blueprint component, inherits from other blueprint component;
- MyCppComponentBase: c++ component;
- MyComponentInheritedFromCppCode: blueprint component, but it inherits from a c++ component.

Notes:
- All 3 components have a float variable.
- The default value of these variables are 0.
- The MyActor blueprint defines a new value for these variables in each component: 1
- The level is not changing these values.

Error:
Instead of showing all three components with the value "1", one of them is showing a wrong value: the MyComponentInheritedFromCppCode.

If you click the yellow arrow next to the value, it returns to the correct value "1". But, after restart the editor, the value goes back to "0".