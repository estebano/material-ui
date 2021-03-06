---
title: React Slider component
components: SliderStyled, SliderUnstyled
githubLabel:
  component: Slider
materialDesign: https://material.io/components/sliders
waiAria: 'https://www.w3.org/TR/wai-aria-practices/#slider'
---

# Slider

<p class="description">Schieberegler erlauben es Nutzern, eine Auswahl aus einer Reihe von Werten zu treffen.</p>

[Schieberegler](https://material.io/design/components/sliders.html) spiegeln einen Wertebereich entlang einer Leiste wider, aus dem Benutzer einen einzelnen Wert auswählen können. Sie sind ideal zum Anpassen von Einstellungen wie Lautstärke, Helligkeit oder Anwenden von Bildfiltern.

- 📦 [22 kB gzipped](/size-snapshot) (but only +8 kB when used together with other Material-UI components).

{{"component": "modules/components/ComponentLinkHeader.js"}}

## Kontinuierliche Schieberegler

Continuous sliders allow users to select a value along a subjective range.

{{"demo": "pages/components/slider-styled/ContinuousSlider.js"}}

## Discrete sliders

Discrete sliders can be adjusted to a specific value by referencing its value indicator. By order of demos:

You can generate a mark for each step with `marks={true}`.

{{"demo": "pages/components/slider-styled/DiscreteSlider.js"}}

### Small steps

You can change the default step increment.

{{"demo": "pages/components/slider-styled/DiscreteSliderSteps.js"}}

### Custom marks

You can have custom marks by providing a rich array to the `marks` prop.

{{"demo": "pages/components/slider-styled/DiscreteSliderMarks.js"}}

### Restricted values

You can restrict the selectable values to those provided with the `marks` prop with `step={null}`.

{{"demo": "pages/components/slider-styled/DiscreteSliderValues.js"}}

### Label always visible

You can force the thumb label to be always visible with `valueLabelDisplay="on"`.

{{"demo": "pages/components/slider-styled/DiscreteSliderLabel.js"}}

## Range slider

The slider can be used to set the start and end of a range by supplying an array of values to the `value` prop.

{{"demo": "pages/components/slider-styled/RangeSlider.js"}}

## Slider with input field

In this example an input allows a discrete value to be set.

{{"demo": "pages/components/slider-styled/InputSlider.js"}}

## Benutzerdefinierte Auswahl

Hier einige Beispiele zum Anpassen der Komponente. You can learn more about this in the [overrides documentation page](/customization/components/).

{{"demo": "pages/components/slider-styled/CustomizedSlider.js"}}

## Vertical sliders

{{"demo": "pages/components/slider-styled/VerticalSlider.js"}}

## Track

The track shows the range available for user selection.

### Removed track

The track can be turned off with `track={false}`.

{{"demo": "pages/components/slider-styled/TrackFalseSlider.js"}}

### Inverted track

The track can be inverted with `track="inverted"`.

{{"demo": "pages/components/slider-styled/TrackInvertedSlider.js"}}

## Non-linear scale

You can use the `scale` prop to represent the `value` on a different scale.

In the following demo, the value _x_ represents the value _2^x_. Increasing _x_ by one increases the represented value by factor _2_.

{{"demo": "pages/components/slider-styled/NonLinearSlider.js"}}

## Unstyled slider

{{"demo": "pages/components/slider-styled/UnstyledSlider.js"}}

## Barrierefreiheit

(WAI-ARIA: https://www.w3.org/TR/wai-aria-practices/#slider)

The component handles most of the work necessary to make it accessible. Sie müssen jedoch sicherstellen, dass:

- Each thumb has a user-friendly label (`aria-label`, `aria-labelledby` or `getAriaLabel` prop).
- Each thumb has a user-friendly text for its current value. This is not required if the value matches the semantics of the label. You can change the name with the `getAriaValueText` or `aria-valuetext` prop.
