<template>
  <div class="slidev-layout timeline">
    <div class="timeline-header">
      <slot name="header" />
    </div>
    <div class="timeline-track">
      <div class="timeline-steps">
        <div class="timeline-step">
          <div class="timeline-step-number">01</div>
          <div class="timeline-step-content">
            <slot name="one" />
          </div>
        </div>
        <div class="timeline-step">
          <div class="timeline-step-number">02</div>
          <div class="timeline-step-content">
            <slot name="two" />
          </div>
        </div>
        <div class="timeline-step">
          <div class="timeline-step-number">03</div>
          <div class="timeline-step-content">
            <slot name="three" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
