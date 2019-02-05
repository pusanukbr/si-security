<template lang="pug">
	.info
		ul.info__list
			li( v-for="(post, index) in posts" )
				span.info__list-question {{ post.title }}
				span.info__list-answer {{ post.items }}
</template>



<script>
export default {
	name: 'info_block',
	data(){
		return{
			posts: [
				{title: "Полное ФИО", items: "Писанюк Богдан Романович"},
				{title: "Год рождения", items: "1992"},
				{title: "Место жительства", items: "г-к. Анапа, Россия"},
				{title: "Скайп", items: "pbr150"},
				{title: "Почта", items: "pusanukbr@gmail.com"}
			]
		}
	}
}
</script>




<style lang="scss">

.info{
	position: relative;

	width: 100%;
	padding-bottom: 65px;

	&__list{
		margin: 0;
		padding: 0;

		li{
			display: flex;
			width: 100%;
			margin-bottom: 25px;

			list-style: none;
		}

		&-question{
			display: flex;
			margin-right: 15px;

			font-size: 23px;
			font-weight: 700;
			color: #2f1b15;
		}

		&-answer{
			position: relative;

			flex: 1;
			padding-left: 15px;

			font-family: 'Courier New', arial;
			font-size: 30px;
			color: #2f1b15;
			line-height: 0;

			background-image: url("../assets/line.png");
			background-position: 0 100%;
			background-size: contain;
			background-repeat: repeat-x;
		}
	}
}

</style>

