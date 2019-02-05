<template lang="pug">
	.date
		span.date__question Дата заполнения
		span.date__answer 05.03.2019
</template>

<style lang="scss">

.date{
	position: relative;
	
	display: flex;
	width: 100%;
	padding-bottom: 70px;

	&__question{
		display: flex;
		margin-right: 15px;

		font-size: 23px;
		font-weight: 700;
		color: #2f1b15;
	}

	&__answer{
		position: relative;

		font-family: 'Courier New', arial;
		font-size: 30px;
		color: #2f1b15;
		line-height: 0;

		background-image: url("../assets/line.png");
		background-position: 0 100%;
		background-repeat: repeat-x;
	}
}

</style>

