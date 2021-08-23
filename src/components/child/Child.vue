<script>
export default {
  name: 'Child',
}
</script>

<template>
  <div :class="$style.main">
    <p :class="$style.copy">
      This is a child component.  Note how both the parent and child components
      use the same CSS class names for their elements ("main" and "copy"), but
      the parent's styling doesn't cascade to the child's styling.
    </p>
    <p :class="$style.copy">
      This is called scoping and effectively negates the CSS cascade.  When
      working with components, <strong>the component is the primitive</strong>.
      This means that a component should be responsible for its own styling and
      should not pollute other components.
    </p>
    <p :class="$style.copy">
      There are things to watch out for though.  For example, "text-align"
      cascades implicitly, so components should declare their "text-align"
      property for security.
    </p>
    <p :class="$style.copy">
      If a component's styles should change from their defaults, this should
      be an option provided as a prop so that the reason for the style change
      is easy to track and change on a contextual basis.
    </p>
    <p :class="$style.copy" class="some_non-scoped_class">
      This paragraph inherits its styles from outside of the component.  That
      means that this component could potentially break if a style change is made
      elsewhere in the application.
    </p>
  </div>
</template>

<style module>
.main {
  background-color: #fff;
  padding: 1rem;
  color: #fff;
  margin: 0.5rem;
  box-shadow: 0 0 0 0.5rem #fff;
  border: thin solid #000;
}

.copy {
  color: #000;
  font-family: Times, serif;
  text-align: left;
}
</style>

