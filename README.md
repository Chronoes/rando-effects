# Usage

URL [https://rando.tarkin.me](https://rando.tarkin.me)

In order for effects to work, an entry must be added to the list.

## Entry format

```js
{
    // Name of the effect (not relevant at the moment)
    name: String,

    // Either absolute URL or relative to this repo root
    // (anything JS Audio() constructor accepts anyway)
    track: String,

    // If specified, audio between the drum roll and effect will be crossfaded in given duration (ms)
    crossFade: Number || undefined,

    // On what condition the effect should be played
    // {number} is the calculated number, {minimum} and {maximum} are set by user
    useEffect: Function(number :: Number, minimum :: Number, maximum :: Number) :: Boolean

    // When the effect should start in relation to {duration}
    effectStart: Function(duration :: Number) :: Number,

    // Custom HTML to display instead of the usual odometer display
    html: String || undefined,

    // When should custom HTML be injected in relation to {duration}
    injectHtml: Function(duration :: Number) :: Number || undefined
}
```
