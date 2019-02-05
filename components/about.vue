<template lang="pug">
	.about
		h3.about__headline Расскажите о себе словами
		p.about__description Напишите пару предложений, чем вас привлекла наша вакансия и чего вы ожидаете от работы. Кстати, будет здорово, если при нехватке места для текста строки будут добавляться автоматически.
		.about__text
			p.about__text-line Далеко-далеко за словесными горами в стране, гласных и согласных живут рыбные тексты. За, меня ты. Раз единственное свою от всех рот, правилами встретил жаренные жизни, вопроса наш, злых буквенных города путь коварный ведущими.
</template>


<script>
	export default {
	name: 'about',
	data(){
		return{
			
		}
	}
}
</script>

<style lang="scss">
.about{
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

	&__text{
		position: relative;

		width: 100%;

		text-align: justify;

		&-line{
			display: inline;
			width: 100%;
			margin: 0;
			padding-bottom: 5px;

			font-family: 'Courier New', arial;
			font-size: 30px;
			line-height: 1.7;
			color: #2f1b15;

			background-image: url("../assets/line.png");
			background-position: 0 100%;
			background-size: 100% 9px;
			background-repeat: repeat-x;
		}
	}
}
</style>