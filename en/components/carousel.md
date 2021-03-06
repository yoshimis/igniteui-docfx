---
title: Carousel Component
_description: Use Ignite UI for Angular Carousel component to navigate through a collection of slides, cards or page-based interfaces with endless programmatic features.
_keywords: Ignite UI for Angular, UI controls, Angular widgets, web widgets, UI widgets, Angular, Native Angular Components Suite, Native Angular Controls, Native Angular Components Library, Angular Carousel component, Angular Carousel control
---

##Carousel
<p class="highlight">Use the Ignite UI for Angular Carousel component to browse or navigate through a collection of slides, including image galleries, cards, onboarding tutorials, or page-based interfaces. The carousel can be used as a full-screen element or situated inside another component. Slides can be programmed to change at defined intervals in slide-show mode, or set to be scrolled manually by users. Programmatic features of the control include raising an event when a slide is changed, added, or removed.</p>
<div class="divider"></div>

### Carousel Demo
<div class="sample-container" style="height: 800px">
    <iframe seamless width="100%" height="100%" frameborder="0" src="{environment:demosBaseUrl}/carousel"></iframe>
</div>
<div class="divider--half"></div>

### Usage
```html
<igx-carousel [interval]="interval" [pause]="shouldPause" [loop]="shouldLoop">
    <igx-slide *ngFor="let slide of slides;" [active]="slide.active">
        <img [src]="slide.image">
    </igx-slide>
</igx-carousel>
```
<div class="divider--half"></div>

###API
<div class="divider--half"></div>

#### Carousel (igx-carousel)
<div class="divider--half"></div>

| Name   |      Type      |  Description |
|:----------|:-------------:|:------|
| `loop` |  boolean | Should the carousel wrap back to the first slide after it reaches the last. Defaults to `true`. |
| `pause` | boolean | Should the carousel stop playing on user interaction. Defaults to `true`.  |
| `interval` | number | The amount of time in milliseconds between slides transition. |
| `navigation` | boolean | Controls should the carousel render the left/right navigation buttons. Defaults to `true`. |
| `total` | number | The number of slides the carousel currently has.  |
| `current` | number | The index of the slide currently showing. |
| `isPlaying` | boolean | Returns whether the carousel is paused/playing. |
| `isDestroyed` | boolean | If the carousel is destroyed (`ngOnDestroy` was called) |
| `onSlideChanged` | event | Emitted on slide change |
| `onSlideAdded` | event | Emitted when a slide is being added to the carousel |
| `onSlideRemoved`| event | Emitted whe a slide is being removed from the carousel |
| `onCarouselPaused` | event | Emitted when the carousel is pausing. |
| `onCarouselPlaying`| event | Emitted when the carousel starts/resumes playing. |
| `play()` | void | Emits `onCarouselPlaying` event and starts the transition between slides. |
| `stop()` | void | Emits `onCarouselPaused` event and stops the transition between slides. |
| `prev()` | void | Switches to the previous slide. Emits `onSlideChanged` event. |
| `next()` | void | Switches to the next slide. Emits `onSlideChanged` event. |
| `add(slide: IgxSlide)` | void | Adds a slide to the carousel. Emits `onSlideAdded` event. |
| `remove(slide: IgxSlide)` | void | Removes an existing slide from the carousel. Emits `onSlideRemoved` event. |
| `get(index: Number)` | IgxSlide or void | Returns the slide with the given index or null. |
| `select(slide: IgxSlide, direction: Direction)`| void | Selects the slide and the direction to transition to. Emits `onSlideChanged` event. |

#### Slide (igx-slide)
<div class="divider--half"></div>

| Name   |      Type      |  Description |
|:----------|:-------------:|:------|
| `index` |  number | The index of the slide inside the carousel. |
| `direction` |  Direction | The direction in which the slide should transition. Possibly values are `NONE`, `NEXT`, `PREV` |
| `active`| boolean | Whether the current slide is active, i.e. the one being currently displayed by the carousel. |
