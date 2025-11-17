<template>
  <div>
    <h1>Slot examples</h1>
    <slot name="header">
      <h2>Default Header</h2>
    </slot>
    <slot>
      <p>This is the default content.</p>
    </slot>
    <slot name="footer">
      <h4>Default Footer</h4>
    </slot>
  </div>
</template>
