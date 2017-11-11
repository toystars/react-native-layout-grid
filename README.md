# react-native-layout-grid

[![npm](https://img.shields.io/npm/v/react-native-layout-grid.svg)](https://www.npmjs.com/package/react-native-layout-grid) [![Downloads](https://img.shields.io/npm/dt/react-native-layout-grid.svg)](https://www.npmjs.com/package/react-native-layout-grid) [![Licence](https://img.shields.io/npm/l/react-native-layout-grid.svg)](https://www.npmjs.com/package/react-native-layout-grid)

> Simple Grid Layout for react-native

<br>

![grid](https://user-images.githubusercontent.com/16062709/32684146-2c768858-c681-11e7-85cd-6455c8f0d6ec.gif)


## Installation

``` bash
$ npm install react-native-layout-grid --save
```
or use yarn

``` bash
$ yarn add react-native-layout-grid
```


## Usage
The snippet below shows how the component can be used

```javascript

import React, { Component } from 'react';
import {
  Platform,
  StyleSheet,
  Text,
  View,
} from 'react-native';
import GridLayout from 'react-native-layout-grid';

export default class App extends Component<{}> {

  renderGridItem = (item) => (
    <View style={styles.item}>
      <View style={styles.flex} />
      <Text style={styles.name}>
        {item.name}
      </Text>
    </View>
  );

  render() {
    const items = [];
    for (let x = 1; x <= 30; x++) {
      items.push({
        name: `Grid ${x}`
      });
    }
    return (
      <View style={styles.container}>
        <Text style={styles.welcome}>
          Grid Layout
        </Text>
        <View style={styles.flex}>
          <GridLayout
            items={items}
            itemsPerRow={3}
            renderItem={this.renderGridItem}
          />
        </View>
      </View>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    marginTop: 20,
    backgroundColor: '#F5FCFF',
  },
  welcome: {
    fontSize: 20,
    textAlign: 'center',
    margin: 10,
  },
  flex: {
    flex: 1,
  },
  item: {
    height: 150,
    backgroundColor: '#CCCCCC',
    padding: 10,
  },
  name: {
    fontSize: 12,
    textAlign: 'center',
    color: '#000000'
  },
});
    
```

## Props

| Prop        | Required   | Type    | Purpose  |
| ------------- |-------------|-------|-----------|
| items | Yes   | Array | Items to display in Grid |
| itemsPerRow | Yes   | Number | Number of items on each Grid row |
| renderItem | Yes   | Function | Single item rendering function |


## Contributing

Contributions are **welcome** and will be fully **credited**.

Contributions are accepted via Pull Requests on [Github](https://github.com/toystars/react-native-layout-grid).


### Pull Requests

- **Document any change in behaviour** - Make sure the `README.md` and any other relevant documentation are kept up-to-date.

- **Consider our release cycle** - We try to follow [SemVer v2.0.0](http://semver.org/). Randomly breaking public APIs is not an option.

- **Create feature branches** - Don't ask us to pull from your master branch.

- **One pull request per feature** - If you want to do more than one thing, send multiple pull requests.

- **Send coherent history** - Make sure each individual commit in your pull request is meaningful. If you had to make multiple intermediate commits while developing, please [squash them](http://www.git-scm.com/book/en/v2/Git-Tools-Rewriting-History#Changing-Multiple-Commit-Messages) before submitting.


## Issues

Check issues for current issues.

## Contributors

[Mustapha Babatunde](https://twitter.com/iAmToystars)
 

## License

The MIT License (MIT). Please see [LICENSE](LICENSE) for more information.
