<template lang="pug">
	.checkbox
		h3.checkbox__headline Расскажите о себе чекбоксами
		p.checkbox__description Отметьте чекбоксами пункты, которые соответствуют вашим скиллам. Кстати, отсутствие опыта не означает, что у вас меньше шансов стать одним из наших товарищей. Это означает, что вы будете получать те задачи, с которыми гарантировано будете справляться.
		.checkbox__box
			ul.checkbox__list
				li( v-for="(check, index) in checks" )
					input.checkbox__list-check( type="checkbox" v-bind:id="check.id" v-bind:checked='check.checked')
					label.checkbox__list-text( :for="check.id") {{check.text}}
</template>


<script>
	export default {
	name: 'checkbox',
	data(){
		return{
			checks: [
				{id: "check-1", text: "БЭМ/OOCSS", checked: "checked"},
				{id: "check-2", text: "Pug (Jade)", checked: "checked"},
				{id: "check-3", text: "Stylus/LESS/SASS", checked: "checked"},
				{id: "check-4", text: "Работаю с SVG", checked: "checked"},
				{id: "check-5", text: "Верстаю семантично", checked: "checked"},
				{id: "check-6", text: "Accessibility (A11Y)", checked: "checked"},
				{id: "check-7", text: "ES2015/ES2016", checked: "checked"},
				{id: "check-8", text: "Gulp/GRUNT", checked: "checked"},
				{id: "check-9", text: "Webpack", checked: "checked"},
				{id: "check-10", text: "Дружу с WebGL", checked: ""},
				{id: "check-11", text: "jQuery ", checked: "checked"},
				{id: "check-12", text: "Знаю/изучаю VUE", checked: "checked"},
				{id: "check-13", text: "Знаю/изучаю React", checked: ""},
				{id: "check-14", text: "Знаю/изучаю Node.js", checked: ""},
				{id: "check-15", text: "Использую Git", checked: "checked"},
				{id: "check-16", text: "С глазомером всё ок", checked: "checked"},
				{id: "check-17", text: "Читаю habr.com", checked: "checked"},
				{id: "check-18", text: "Я ленивый(-ая)", checked: ""},
				{id: "check-19", text: "У меня хороший английский", checked: ""},
			]
		}
	}
}
</script>

<style lang="scss">
.checkbox{
	position: relative;

	width: 100%;
	padding-bottom: 65px;

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
		margin: 0;
		padding: 0;

		column-count: 3;
		column-gap: 35px;

		li{
			position: relative;

			display: flex;
			align-items: center;
			width: 100%;
			margin-bottom: 15px;

			list-style: none;
			font-family: 'PT Sans';
		}

		&-check{
			z-index: 3;

			width: 15px;
			height: 15px;
			margin-right: 10px;

			opacity: 0;
			cursor: pointer;
			&:checked + .checkbox__list-text{
				&:before{
					position: absolute;
					top: calc(50% - 13.5px);
					left: 1px;
					z-index: 1;

					content: "";
					display: block;
					width: 27px;
					height: 21px;

					background-image: url(../assets/checked.png);
					background-size: contain;
					background-position: top left;
					background-repeat: no-repeat;
				}
			}
		}

		&-text{

			font-size: 21px;
			font-weight: 700;
			color: #000000;

			cursor: pointer;

			&:after{
				position: absolute;
				top: calc(50% - 7.5px);
				left: 0;
				z-index: 1;

				content: "";
				display: block;
				width: 15px;
				height: 15px;

				background-image: url(../assets/checkbox.png);
				background-size: contain;
				background-position: center;
			}
		}
	}
}
</style>