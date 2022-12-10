<template>
  <div class="bg">
    <div class="container flex-row">
      <div class="d-flex mb-3 w-100">
        <div class="input-group w-50">
          <input type="number" class="form-control" style="text-align:right" id="foot" @input="feetToMeters" v-model="feet" aria-label="Username" aria-describedby="basic-addon1">
          <div class="input-group-text d-inline-block" style="width: 35%">Футы</div>
        </div>
        <div class="input-group w-50">
          <div class="input-group-text d-inline-block" style="width: 35%">Метры</div>
          <input type="number" class="form-control" id="meters" @input="metersToFeet" v-model="meters" aria-label="Username" aria-describedby="basic-addon1">
        </div>
      </div>
    </div>

    <div class="container flex-row">
      <div class="d-flex mb-3 w-100">
        <div class="input-group w-50">
          <input type="number" class="form-control" style="text-align:right" id="miles" @input="milesToKilometers" v-model="miles" aria-label="Username" aria-describedby="basic-addon1">
          <div class="input-group-text d-inline-block" style="width: 35%">Мили</div>
        </div>
        <div class="input-group w-50">
          <div class="input-group-text d-inline-block" style="width: 35%">Километры</div>
          <input type="number" class="form-control" id="kilometers" @input="kilometersToMiles" v-model="kilometers" aria-label="Username" aria-describedby="basic-addon1">
        </div>
      </div>
    </div>

    <div class="container flex-row">
      <div class="d-flex mb-3 w-100">
        <div class="input-group w-50">
          <input type="number" class="form-control" style="text-align:right" id="celsius" @input="celsiusToFahrenheit" v-model="celsius" aria-label="Username" aria-describedby="basic-addon1">
          <div class="input-group-text d-inline-block" style="width: 35%">Цельсии</div>
        </div>
        <div class="input-group w-50">
          <div class="input-group-text d-inline-block" style="width: 35%">Фаренгейты</div>
          <input type="number" class="form-control" id="fahrenheit" @input="fahrenheitToCelsius"   v-model="fahrenheit" aria-label="Username" aria-describedby="basic-addon1">
        </div>
      </div>
    </div>

    <div class="container flex-row">
      <div class="d-flex mb-3 w-100">
        <div class="input-group w-50">
          <input type="number" class="form-control" style="text-align:right" @input="degreesToRadians" id="degrees" v-model="degrees" aria-label="Username" aria-describedby="basic-addon1">
          <div class="input-group-text d-inline-block" style="width: 35%">Градусы</div>
        </div>
        <div class="input-group w-50">
          <div class="input-group-text d-inline-block" style="width: 35%">Радианы</div>
          <input type="number" class="form-control" id="radians" @input="radiansToDegrees" v-model="radians" aria-label="Username" aria-describedby="basic-addon1">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainConverter',
  data: () => ({
    feet: 0,
    meters: 0,
    miles: 0,
    kilometers: 0,
    degrees: 0,
    radians: 0,
    celsius: 0,
    fahrenheit: 0,
  }),
  // Методы-формулы перевода из одной единицы измерения в другую
  methods: {
    feetToMeters() {
      this.meters = this.feet * 3.281;
    },
    metersToFeet() {
      this.feet = this.meters / 3.281;
    },
    milesToKilometers() {
      this.kilometers = this.miles * 1.852;
    },
    kilometersToMiles() {
      this.miles = this.kilometers / 1.852;
    },
    degreesToRadians() {
      this.radians = this.degrees * (Math.PI / 180);
    },
    radiansToDegrees() {
      this.degrees = this.radians * (180 / Math.PI);
    },
    celsiusToFahrenheit() {
      this.fahrenheit = this.celsius * 1.8 + 32;
    },
    fahrenheitToCelsius() {
      this.celsius = (this.fahrenheit - 32) / 1.8;
    },
  },
};
</script>


