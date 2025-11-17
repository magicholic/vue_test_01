<template>
  <div>
    <h1>Slot example</h1>
    <slot name="header">
      <h4>Default Header</h4>
    </slot>
    <slot>
      <p>This is the default content.</p>
    </slot>
    <slot name="footer">
      <h4>Default Footer</h4>
    </slot>
  </div>
</template>
