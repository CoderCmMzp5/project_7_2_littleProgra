<template>
	<view>
		<block v-for="(weeks, week) in canlender.weeks" :key="week">
			<view class="uni-calender__body-date-week">
				<block v-for="(day, index) in weeks" :key="index">
					<view class="uni-calender__date" :class="{
							'uni-calender__disable': canlender.month !== day.month || day.disable,
							'uni-calender__date-current':
								(day.date == canlender.date || day.checked) &&
								canlender.month == day.month &&
								!day.disable,
							'uni-calender__lunar': lunar,
							'uni-calender__active': day.isDay,
							'uni-calender__is-day': day.isDay
						}"
					 @tap="
							selectDays(
								week,
								index,
								canlender.month === day.month,
								day.disable,
								canlender.lunar
							)
						">
						<view class="uni-calender__circle-box">
							<view class="uni-calender__data-have">{{ day.date }}</view>
							<view v-if="lunar" class="uni-calender__lunar">{{ day.lunar }}</view>
							<view v-if="day.have" class="uni-calender__data-circle"></view>
						</view>
					</view>
				</block>
			</view>
		</block>
	</view>
</template>

<script>
	export default {
		name: 'uni-calendar-item',
		props: {
			/**
			 * 当前日期
			 */
			canlender: {
				type: null,
				default: () => {
					return {};
				}
			},
			lunar: {
				type: Boolean,
				default: false
			}
		},
		data() {
			return {};
		},
		created() {},
		methods: {
			selectDays(week, index, ischeck, isDay, lunar) {
				this.$emit('selectDays', {
					week,
					index,
					ischeck,
					isDay,
					lunar
				});
			}
		}
	};
</script>

<style lang="scss">
	.uni-calender__body-date-week {
		display: flex;
		width: 100%;
		border-bottom: 1px #f5f5f5 solid;

		&:last-child {
			border: none;
		}

		// 日期的样式
		.uni-calender__date {
			position: relative;
			width: 100%;
			text-align: center;
			display: flex;
			justify-content: center;
			align-items: center;
			color: #000;
			background: #fff;
			// line-height: 100upx;
			box-sizing: border-box;
			padding: 20upx 0;
			line-height: 1.5;

			.uni-calender__lunar {
				font-size: 20upx;
				color: #000;
			}

			.uni-calender__circle-box {
				display: flex;
				flex-direction: column;
				justify-content: center;
				align-items: center;
				width: 80upx;
				height: 80upx;
				flex-shrink: 0;
				border-radius: 50%;
				transition: all 0.2s;
				
			}

			&.uni-calender__lunar {
				// 			padding: 20upx 0;
				// 			line-height: 1.5;
			}

			// 本月禁止的样式
			&.uni-calender__disable {
				color: #d4d4d4;

				.uni-calender__lunar {
					color: #d4d4d4;
				}
			}

			&.uni-calender__is-day {
				color: #222;
				font-weight: 500;
			}

			&.uni-calender__is-day .uni-calender__lunar {
				color: #fd2e32;
			}

			// 当前选中
			&.uni-calender__date-current {
				// background: #000;
				color: #222;
				box-sizing: border-box;

				.uni-calender__circle-box {
					background: #FFE500;
				}

				&.uni-calender__active {}

				.uni-calender__lunar {
					color: #fff;
				}
			}

			.uni-calender__data-circle {
				position: absolute;
				// bottom: 10rpx;
				top: 20upx;
				right: 10upx;
				// margin: auto;
				width: 10rpx;
				height: 10rpx;
				border-radius: 50%;
				background: #ff5a5f;
				z-index: 10;
				
				bottom: 0;
				background-color: #FFE500;
				height: 80upx;
				width: 80upx;
			}
			.uni-calender__data-have{
				position: absolute;
				border-radius: 50%;
				z-index: 100;
				height: 80upx;
				width: 80upx;
				line-height: 80upx;
				text-align: center;
			}
		}
	}
	.uni-calender__body-date-week:nth-of-type(2){
		.uni-calender__data-circle {
			position: absolute;
			// bottom: 10rpx;
			top: 20upx;
			right: 10upx;
			// margin: auto;
			width: 10rpx;
			height: 10rpx;
			border-radius: 50%;
			background: #ff5a5f;
			z-index: 10;
			
			bottom: 0;
			background-color: #f5f5f5;
			height: 80upx;
			width: 80upx;
			color: red;
		}
	}
</style>
