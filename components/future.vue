<template lang="pug">
	.future
		h3.future__headline Какие у вас планы на будущее?
		p.future__description Этот ответ ни на что не повлияет. Не беда, если в будущем ваши
		.future__box
			ul.future__list
				li( v-for="(radio, index) in radios" )
					input.future__list-check( name="future" type="radio" v-bind:id="radio.id" v-bind:checked='radio.checked')
					label.future__list-text( :for="radio.id") {{radio.text}}
</template>


<script>
	export default {
	name: 'future',
	data(){
		return{
			radios: [
				{id: "radio-1", text: "Верстать", checked: ""},
				{id: "radio-2", text: "Прокачиваться в JS", checked: "checked"},
				{id: "radio-3", text: "Менеджерство", checked: ""},
				{id: "radio-4", text: "Другое", checked: ""}
			]
		}
	}
}
</script>

<style lang="scss">
.future{
	position: relative;

	width: 100%;
	padding-bottom: 80px;

	&__headline{
		width: 100%;
		margin: 0;
		margin-bottom: 20px;

		font-size: 23px;
		font-weight: 700;
		color: #2f1b15;
		line-height: 1;
	}

	&__description{
		width: 100%;
		margin: 0;
		margin-bottom: 25px;

		font-size: 15px;
		color: #3d3d3d;
		line-height: 23px;
	}

	&__list{
		display: flex;
		margin: 0;
		padding: 0;

		li{
			position: relative;

			display: flex;
			align-items: center;
			margin-bottom: 15px;
			margin-right: 20px;

			list-style: none;
			font-family: 'PT Sans';
		}

		&-check{
			z-index: 3;

			width: 25px;
			height: 25px;
			margin-right: 10px;

			opacity: 0;
			cursor: pointer;
			&:checked + .future__list-text{
				&:before{
					position: absolute;
					top: calc(50% - 6px);
					left: 7px;
					z-index: 1;

					content: "";
					display: block;
					width: 12px;
					height: 12px;

					background-image: url(../assets/dot.png);
					background-size: contain;
					background-position: top left;
					background-repeat: no-repeat;
				}
			}
		}

		&-text{

			font-size: 20px;
			font-weight: 700;
			color: #000000;

			cursor: pointer;

			&:after{
				position: absolute;
				top: calc(50% - 12.5px);
				left: 0;
				z-index: 1;

				content: "";
				display: block;
				width: 25px;
				height: 25px;

				background-image: url(../assets/radio.png);
				background-size: contain;
				background-position: center;
				background-repeat: no-repeat;

			}
		}
	}
}
</style>