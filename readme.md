vcalc is an Sass function for calculate unit from px to vw or vmin.

## Install
```
$ npm install --save-dev vcalc
```


```scss
@import 'vcalc';
```

Set variable `$base-v-size` as you want, default sets `375` (iPhone6).
```
$base-v-size: 320;
```

## Useage

|Name|Arg1|Arg2|
|---|---|---|
|vmin-calc|$values: px based value|$base: base viewport size|
|vw-calc|$values: px based value|$base: base viewport size|


```scss
// $base-v-size: 375;
{
  font-size: vmin-calc(16px);
}
```

Will be `4.26667vmin`, which means

|Screen width|4.26667vmin In px|
|---|---|
|414px|18px|
|375px||16px|
|320px|14px|

Also can pass multiple values

```scss
{
  margin: vmin-calc(10px 20px 30px 40px);
}
```
