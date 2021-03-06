# tvt-pagination

A long list can be divided into several pages using `Pagination`, and only one page will be loaded at a time.


### Getting started

```sh
yarn add tvt-pagination
```

![screen_shot](./assets/screen_shot.png)


### Example

```js
import React from 'react';
import Pagination from 'tvt-pagination';

export default () => (
  <Pagination
    defaultCurrent={1}
    total={50}
  />
);
```

```js
import React from 'react';
import { Text } from 'react-native';
import Pagination from 'tvt-pagination';

export default () => (
  <Pagination
    size="small"
    total={50}
    prevIcon={
      <Text>Prev</Text>
    }
    nextIcon={
      <Text>Next</Text>
    }
  />
);
```

```js
import React from 'react';
import Pagination from 'tvt-pagination';

export default () => (
  <Pagination
    total={50}
    defaultCurrent={1}
    defaultPageSize={5}
    onChange={(page, pageSize) => alert(`${page} ${pageSize}`)}
  />
);
```


### API

| Property          | Description | Type | Default |
| -----------       | ----------- | ----------- | ----------- |
| defaultCurrent    | Default initial page number | number | 1 |
| defaultPageSize   | Default number of data items per page | number | 10 |
| disabled          | Disable pagination | boolean | |
| total             | Total number of data items | number | 0 |
| onChange          | Called when the page number is changed, and it takes the resulting page number and pageSize as its arguments | function(page, pageSize) | |
| size              | Specify the size of `Pagination`, can be set to `small` | default | middle | small |
| borderColor       | Border color button pagination | string | #d9d9d9 |
| borderColorActive | Border color button current pagination | string | #1890ff |
| activeOpacity     | Determines what the opacity of the wrapped view should be when touch is active | number | 1 |
| prevIcon          | Set the icon prev | ReactNode | |
| nextIcon          | Set the icon next | ReactNode | |
| styleBox          | Style for box button | [ViewStyleProps](https://reactnative.dev/docs/view-style-props#docsNav) | |
| style             | Style for `Pagination` | [ViewStyleProps](https://reactnative.dev/docs/view-style-props#docsNav) | |
| testID            | Used to locate this view in end-to-end tests | string | |