# Google-Adsense
Show google ads using Angular 9

#### Add adsense code

Use the standard AdSense code somewhere in your `<head></head>` as you [normally would](https://support.google.com/adsense/answer/7477845)

```html
<script async src=//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js></script>
```

#### Import NgModule

Add GoogleAdsenseModule to the imports of your NgModule
```
@NgModule({
  imports: [
    // shown passing global defaults (optional)
    AdsenseModule.forRoot({
      adClient: 'ca-pub-9010581920864857',
      adSlot: 1795662914,
    }),
    ...
```

#### Show Ad

Uses global defaults which can be overriden via inputs

```html
<app-google-adsense></app-google-adsense>
```

## Inputs

| input        | type          | description                                                           |
| ------------ | ------------- | --------------------------------------------------------------------- |
| adClient     | string        | account ca-pub-XXXXXXXXXXXXXXXX                                       |
| adSlot       | string/number | ad slot/number                                                        |
| adFormat     | string        | adsense ad format                                                     |
| adRegion     | string        | older adsense code to make all ads on page the same                   |
| display      | string        | element display style                                                 |
| height       | number        | element height in px                                                  |
| width        | number        | element width in px                                                   |
| layout       | string        | used for in-feed ads                                                  |
| layoutKey    | string        | used for in-feed ads                                                  |
| pageLevelAds | boolean       | enable page-level ads                                                 |
| timeOutRetry | boolean       | on first load sometimes adsense is not ready. retry's push after x ms |
| adtest       | string        | sets up some sort of google test ad                                   |
| className    | string        | add custom class names to the "ins" element                           |

```html
<app-google-adsense
  [adClient]="'ca-pub-9010581920864857'"
  [adSlot]="1795662914"
  [display]="'inline-block'"
  [width]="320"
  [height]="108"
></app-google-adsense>
```
