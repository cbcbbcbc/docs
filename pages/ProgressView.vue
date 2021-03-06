<template lang="pug">
  component-view(v-bind:doc="doc")
</template>

<script>
  export default {
    data () {
      return {
        doc: {
          component: 'progress',
          edit: 'ProgressView',
          title: 'Progress',
          desc: 'The <code>v-progress-circular</code> and <code>v-progress-linear</code> components are used to convey data visually to users. They can also represent an indeterminate amount, such as loading or processing. These components contains a slot that is centered within the component container.',
          examples: [
            { header: 'Default', file: 'progress-circular/1', desc: 'By default, progress circular uses the applications secondary color.' },
            { header: 'Colored', file: 'progress-circular/2', desc: 'Alternate colors can be applied.' },
            { header: 'Indeterminate', file: 'progress-circular/3', desc: 'An indeterminate progress circular animates forever.' },
            { header: 'Size & Width', file: 'progress-circular/4', desc: 'The progress circular component can have an altered width and size.' },
            { header: 'Rotate', file: 'progress-circular/5', desc: 'The progress origin can be rotated.' },
            { header: 'Determinate', file: 'progress-linear/1', desc: 'The progress linear component can have a determinate state modified by v-model.' },
            { header: 'Indeterminate', file: 'progress-linear/2', desc: 'Just as with the progress circular component, progress linear has an indeterminate state.' },
            { header: 'Buffer', file: 'progress-linear/3', desc: 'A buffer state represents two values simultaneously. The primary value is controled by the model, whereas the buffer is controlled by the <code>buffer-value</code> prop.'},
            { header: 'Query Indeterminate and Determinate', file: 'progress-linear/4', desc: 'To query state is controlled by the truthiness of indeterminate with the query prop set to true.'},
            { header: 'Custom height and contextual colors', file: 'progress-linear/5', desc: 'A custom height or contextual color can be applied to a progress bar. The bars primary color is your applications primary color.'},
          ],
          props: {
            'v-progress-circular': {
              params: [
                [
                  'fill',
                  'String',
                  "[indeterminate ? 'none' : 'transparent']",
                  'Sets the fill color of the circle'
                ],
                [
                  'indeterminate',
                  'Boolean',
                  'False',
                  'Never stops rotating. Use when loading progress is unknown.'
                ],
                [
                  'rotate',
                  'Number',
                  '0',
                  'Rotates the circle start point in deg'
                ],
                [
                  'size',
                  'Number',
                  '32',
                  'Sets the diameter of the circle in pixels'
                ],
                [
                  'width',
                  'Number',
                  '4',
                  'Sets the stroke of the circle in pixels'
                ]
              ],
              model: {
                types: ['Number'],
                default: '0',
                description: 'The percentage value for current progress'
              }
            },

            'v-progress-linear': {
              params: [
                [
                  'buffer',
                  'Boolean',
                  'False',
                  'Designates whether the buffer bar is shown'
                ],
                [
                  'buffer-value',
                  'Number',
                  'None',
                  'The percentage value for the buffer'
                ],
                [
                  'height',
                  'number',
                  '7',
                  'The height of the progress bar'
                ],
                [
                  'indeterminate',
                  'Boolean',
                  'False',
                  'Sets the indeterminate state of the component. Use when loading progress is unknown'
                ],
                [
                  'active',
                  'Boolean',
                  'True',
                  'When disabled, the component will shrink up'
                ],
                [
                  'query',
                  'Boolean',
                  'False',
                  'Sets the query state of the component'
                ],
                [
                  'secondary',
                  'Boolean',
                  'False',
                  'Sets the progress context to "Secondary"'
                ],
                [
                  'success',
                  'Boolean',
                  'False',
                  'Sets the progress context to "Success"'
                ],
                [
                  'info',
                  'Boolean',
                  'False',
                  'Sets the progress context to "Info"'
                ],
                [
                  'warning',
                  'Boolean',
                  'False',
                  'Sets the progress context to "Warning"'
                ],
                [
                  'error',
                  'Boolean',
                  'False',
                  'Sets the progress context to "Error"'
                ],
              ],
              model: {
                types: ['Number'],
                default: '0',
                description: 'The percentage value for current progress'
              }
            }
          },
          slots: {
            'v-progress-circular': {
              default: true
            }
          }
        }
      }
    }
  }
</script>
