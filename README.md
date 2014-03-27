# plan-icons

Various style components for our plans

## .PlanBadge

Plan icon next to the plan name. This can be made horizontal with
`.PlanBadge--horizontal`.

```html
<div class="PlanBadge">
  <div class="PlanBadge-icon">...</div>
  <h3 class="PlanBadge-name">Project</h3>
</div>
```

## .PlanWheel

The SVG version of our plan icons that can be animated. You'll need
to include the SVG in the HTML.

```html
<svg class="PlanWheels">
  <circle class="PlanWheel green" cx="25" cy="25" r="17" />
  <circle class="PlanWheel darkGreen quarter" cx="25" cy="25" r="17" />
</svg>
```

You'll need to stack two circles to create the icon. The modifiers for the wheel are:

* bronze
* green
* darkGreen
* diamond
* empty
* quarter
* half
* threeQuarter

Adding and removing the `empty`, `quarter`, `half`, and `threeQuarter` modifiers will animate
the SVG using CSS transitions. It does this using stroke-offset. This means you can set these
modifiers on waypoints to trigger animation.

You can use the wheels within `.PlanBadge`:

```html
<div class="PlanBadge">
  <svg class="PlanBadge-icon PlanWheels">
    <circle class="PlanWheel green empty" waypoint-remove="empty" waypoint-delay="500" cx="25" cy="25" r="17" />
    <circle class="PlanWheel darkGreen quarter empty" waypoint-remove="empty" waypoint-delay="500" cx="25" cy="25" r="17" />
  </svg>
  <h3 class="PlanBadge-name">Developer</h3>
</div>
```

## .PlanIcon

Basic icons that use SVGs as backgrounds. This is used when
you don't need animation in the icon.

```html
<i class="PlanIcon PlanIcon--developer"></i>
```

Compose this within the PlanBadge.

```html
<div class="PlanBadge">
  <i class="PlanBadge-icon PlanIcon PlanIcon--developer"></i>
  <h3 class="PlanBadge-name">Project</h3>
</div>
```

## .PlanBox

The plan details in a white box used on the pricing page. This
is combined with the other components.
