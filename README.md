This is a standalone version of the ScatterplotLayer 

### Usage
```
export MapboxAccessToken=<MapboxPubliAPIToken>
yarn install
npm start
```

### Data format

The Scatterplot Layer takes in paired latitude and longitude coordinated
points and renders them as circles with a certain radius.

```js
import DeckGL, {ScatterplotLayer} from 'deck.gl';

const App = ({data, viewport}) => {

  /**
   * Data format:
   * [
   *   {position: [-122.4, 37.7], radius: 5, color: [255, 0, 0]},
   *   ...
   * ]
   */
  const layer = new ScatterplotLayer({
    id: 'scatterplot-layer',
    data,
    radiusScale: 100,
    outline: false
  });

  return (<DeckGL {...viewport} layers={[layer]} />);
};
```

