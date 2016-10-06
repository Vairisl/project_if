<template>
<input v-model="car.horsePower"/>
<input v-model="car.price"/>
<br/>

Plate number <b>{{car.plateNumber}}</b>
</br>
Horse power <b>{{car.horsePower}}</b>
</br>
Car price <b>{{car.isCheapCar}}</b>
</br>

<span v-if="isCoolCar(car)">Ahujenna</span>

<span v-if="isCheapCar(car)">Cheap as shit</span>

</template>

<script>

export default {
	data () {
		return{
			car: {
				plateNumber: "AA-3333",
				horsePower: 1200,
				price: 9999,
			}
		}
	},
	
	methods: {
		isCoolCar(car){
			return (car.horsePower > 1000) 
		},
		isCheapCar(car){
			return (car.price < 200)
		}
	}
}

</script>

<style>
</style>

