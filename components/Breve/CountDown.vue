<template>
  <div class="countdown">
    <div class="countdown-container">
      <div class="count-item">
        <div class="value">{{ m_days }}</div>
        <div class="label">Dias</div>
      </div>
      <div class="count-item">
        <div class="value">{{ m_hours }}</div>
        <div class="label">Horas</div>
      </div>
      <div class="count-item">
        <div class="value">{{ m_min }}</div>
        <div class="label">Min</div>
      </div>
      <div class="count-item">
        <div class="value">{{ m_seg }}</div>
        <div class="label">Seg</div>
      </div>
    </div>
  </div>
</template>

<script>
import moment from 'moment'

const format = (num) => {
  if (num < 10) {
    return '0' + num;
  }

  return num;
};

export default {
  mounted() {
    this.m_target = moment(this.target);
    this.calculate();
  },
  props: {
    target: {
      type: String,
      default: '2023-01-25 23:35:46',
      required: false,
    },
    interval: {
      type: Number,
      default: 1000,
      required: false,
    }
  },
  data() {
    return {
      m_current: null,
      m_target: '2023-01-25: 23:35:46',
      m_days: '00',
      m_hours: '00',
      m_min: '00',
      m_seg: '00'
    }
  },
  methods: {
    calculate() {
      this._calculate();
      setInterval(() => { this._calculate() }, this.interval);
    },
    _calculate() {
      this.current = moment.duration(this.m_target.diff(moment()));
      this.m_days = format(this.current.days());
      this.m_hours = format(this.current.hours());
      this.m_min = format(this.current.minutes());
      this.m_seg = format(this.current.seconds());
    }
  },
}
</script>

<style scoped>
.countdown {
  margin: 40px 0px;
}

.countdown-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
}

.countdown-container .count-item {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  border: 2px solid var(--primary-color);
  margin: 10px;
  padding: 10px;
  flex-grow: 1;
  background-color: rgba(3, 15, 39, 0.8);
  border-radius: 7px;
}

.countdown-container .count-item .value, 
.countdown-container .count-item .label {
  color: var(--white-color);
}

.countdown-container .count-item .value {
  font-size: 3.5rem;
  font-weight: 700;
  width: 80px;
  text-align: center;
}

.countdown-container .count-item .label {
  font-size: 1.5rem;
  font-weight: 400;
}

@media screen and (max-width: 590px) {
  .countdown-container .count-item .value {
    font-size: 2.2rem;
    width: 50px;
  }

  .countdown-container .count-item .label {
    font-size: 1.2rem;
  }
}

@media screen and (max-width: 475px) {
  .countdown-container .count-item .value {
    font-size: 1.9rem;
    width: 45px;
  }

  .countdown-container .count-item .label {
    font-size: 1rem;
  }
}

@media screen and (max-width: 430px) {
  .countdown-container .count-item {
    padding: 5px;
    margin: 5px;
  }

  .countdown-container .count-item .value {
    font-size: 1.3rem;
    width: 35px;
  }

  .countdown-container .count-item .label {
    font-size: 0.7rem;
  }
}
</style>