# vue-map-filters


![vue-map-filters](https://img.shields.io/npm/v/npm.svg?style=flat-square)

A NPM package port of a pretty useful mapFilters function that @nirazul wrote in [this issue](https://github.com/vuejs/Discussion/issues/405)

#### Why does this exist? 
This is useful DRY (Don't Repeat Yourself) principle application for when you have [**globally** registered filters](https://vuejs.org/v2/guide/filters.html) that you want to implement the a Vue component's scripts rather than its template.

#### Example implementation

```
$ npm install vue-map-getters
```

Then, inside of your Vue component... 

```
<script>

import { mapFilters } from 'vue-map-filters';

export default {
    methods: {
        ...mapFilters(['coolFilter', 'awesomefilter'])
    }
}

</script>
```

Use the `...` spread operator in your component's `methods` hook, just like how you might with the `...mapActions` helper that is built in to Vue! 

Note: similar functionality to `...mapGetters` but should be invoked in `computed`.