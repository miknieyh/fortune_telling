<template>
  <div>
    <b-form inline v-if="show" @submit="onsubmit" @reset="onReset">
      <b-form-group
        id="birth"
        label="생년월일시"
      >
        <b-form-input
          id="birthDay"
          v-model="form.birthDay"
          type="text"
          required
        ></b-form-input>
        <b-form-select
          id="birthTime"
          v-model="form.birthTime"
          :options="times"
          required
        />
      </b-form-group>
    </b-form>
  </div>
</template>

<script>
export default {
  name: 'FortuneSearch',
  data () {
    return {
      form: {
        birthDay: '',
        birthTime: ''
      },
      times: [{ text: 'Select One', value: null },
        { text: '23:30~01:30', value: '자' },
        { text: '01:30~03:30', value: '축' },
        { text: '03:30~05:30', value: '인' },
        { text: '05:30~07:30', value: '묘' },
        { text: '07:30~09:30', value: '진' },
        { text: '09:30~11:30', value: '사' },
        { text: '11:30~13:30', value: '오' },
        { text: '13:30~15:30', value: '미' },
        { text: '15:30~17:30', value: '신' },
        { text: '17:30~19:30', value: '유' },
        { text: '19:30~21:30', value: '술' },
        { text: '21:30~23:30', value: '해' }
      ],
      show: true
    }
  }
}
</script>

<style scoped>

</style>
