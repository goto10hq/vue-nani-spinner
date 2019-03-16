<template>
  <div class="vue-nani-spinner">
    <div class="vue-nani-spinner-spinner" :style="spinnerStyle"></div>
    <div class="vue-nani-spinner-text" :style="textStyle" v-if="text.length > 0">{{ text }}</div>
  </div>
</template>
<script>
  var isNumber = function (n) {
    return !isNaN(parseFloat(n)) && isFinite(n)
  }

  export default {
    name: 'spinner',
    props: {
      direction: {
        type: Number,
        default: 1,
        validator: v => {
          return v == 1 || v == -1
        }
      },
      size: {
        type: Number,
        default: 32
      },
      lineSize: {
        type: Number,
        default: 3
      },
      lineBackground: {
        type: String,
        default: '#EEEEEE'
      },
      lineColor: {
        type: String,
        default: '#2196F3'
      },
      speed: {
        type: Number,
        default: 0.8
      },
      textSpacing: {
        type: Number,
        default: 4
      },
      text: {
        type: String,
        default: ''
      },
      textSize: {
        type: [Number, String],
        default: 13
      },
      textColor: {
        type: String,
        default: '#555555'
      }
    },
    computed: {
      textFontSize () {
        return isNumber(this.textSize) ? this.textSize + 'px' : this.textSize
      },
      spinnerStyle () {
        return {
          border: this.lineSize + 'px solid ' + this.lineBackground,
          'border-top': this.lineSize + 'px solid ' + this.lineColor,
          width: this.size + 'px',
          height: this.size + 'px',
          animation: 'vue-nani-spinner-spin' + (this.direction == 1 ? ' ' : '-2 ') + this.speed + 's linear infinite'
        }
      },
      textStyle () {
        return {
          'margin-top': this.textSpacing + 'px',
          color: this.textColor,
          'font-size': this.textFontSize + 'px',
          'text-align': 'center'
        }
      }      
    }
  }
</script>
<style lang="scss">
  .vue-nani-spinner-spinner {
    margin: 0 auto;
    border-radius: 100%;
    transition: all 0.3s linear;
  }

  .vue-nani-spinner-text {
      text-align: center;
  }

  @keyframes vue-nani-spinner-spin {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }
  @keyframes vue-nani-spinner-spin-2 {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(-360deg);
    }
  }
</style>