<template>

	<swiper class="swiper" circular :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval"
		:duration="duration">
		<swiper-item v-for="(list,index) in listArray" :key="index">
			<view class="">
				{{index+1}}
			</view>
			<checkbox-group class="chooselist" @change="checkboxChange">
				<checkbox class="choose_item" :value="v.id" :id='v.id' v-for="(v,i) in list.options" :key="v.id"
					:checked="ansArray[index].includes(v.key) ">
					{{v.key}}、{{v.remark}}
				</checkbox>
			</checkbox-group>
		</swiper-item>
	</swiper>
</template>
<script>
	export default {
		data() {
			return {
				ansArray:[],
				listArray: [
					{
					     answers: [
					      {
					       id: 49,
					       remark: null,
					       correct: true,
					      key: "B"
					      },{
					      id: 48,
					      remark: null,
					      correct: true,
					      key: "C"
					     }, {
					      id: 49,
					      remark: null,
					      correct: true,
					      key: "D"
					     }],
					     correct: true,
					     id: 29,
					     name: "对于非司法程序亲子鉴定的描述正确的是(以鉴定父亲儿子关系为例):",
					     options: [{
					      id: 46,
					      key: "A",
					      remark: "可以确定被鉴定人的血型",
					      correct: false,
					     }, {
					      id: 47,
					      key: "B",
					      remark: "可以确定被鉴定人的年龄",
					      correct: false,
					     }, {
					      id: 48,
					      key: "C",
					      remark: " 可以确定被鉴定2人是否亲生关系",
					      correct: true,
					     }, {
					      id: 49,
					      key: "D",
					      remark: "可以确认被鉴定2人性别",
					      correct: true,
					     }],
					     type: "multiple",
					     type_name: "多选",
					   },
					  {
					        answers: [
					         {
					          id: 49,
					          remark: null,
					          correct: true,
					         key: "A"
					         }],
					        correct: true,
					        id: 29,
					        name: "对于非司法程序亲子鉴定的描述正确的是(以鉴定父亲儿子关系为例):",
					        options: [{
					         id: 46,
					         key: "A",
					         remark: "可以确定被鉴定人的血型",
					         correct: false,
					        }, {
					         id: 47,
					         key: "B",
					         remark: "可以确定被鉴定人的年龄",
					         correct: false,
					        }, {
					         id: 48,
					         key: "C",
					         remark: " 可以确定被鉴定2人是否亲生关系",
					         correct: true,
					        }, {
					         id: 49,
					         key: "D",
					         remark: "可以确认被鉴定2人性别",
					         correct: true,
					        }],
					        type: "multiple",
					        type_name: "多选",
					      },
						   {
						       answers: [
						        {
						         id: 49,
						         remark: null,
						         correct: true,
						        key: "B"
						        }, {
						        id: 49,
						        remark: null,
						        correct: true,
						        key: "D"
						       }],
						       correct: true,
						       id: 29,
						       name: "对于非司法程序亲子鉴定的描述正确的是(以鉴定父亲儿子关系为例):",
						       options: [{
						        id: 46,
						        key: "A",
						        remark: "可以确定被鉴定人的血型",
						        correct: false,
						       }, {
						        id: 47,
						        key: "B",
						        remark: "可以确定被鉴定人的年龄",
						        correct: false,
						       }, {
						        id: 48,
						        key: "C",
						        remark: " 可以确定被鉴定2人是否亲生关系",
						        correct: true,
						       }, {
						        id: 49,
						        key: "D",
						        remark: "可以确认被鉴定2人性别",
						        correct: true,
						       }],
						       type: "multiple",
						       type_name: "多选",
						     },
							 {
							      answers: [
							       {
							       id: 48,
							       remark: null,
							       correct: true,
							       key: "A"
							      }, {
							       id: 49,
							       remark: null,
							       correct: true,
							       key: "D"
							      }],
							      correct: true,
							      id: 29,
							      name: "对于非司法程序亲子鉴定的描述正确的是(以鉴定父亲儿子关系为例):",
							      options: [{
							       id: 46,
							       key: "A",
							       remark: "可以确定被鉴定人的血型",
							       correct: false,
							      }, {
							       id: 47,
							       key: "B",
							       remark: "可以确定被鉴定人的年龄",
							       correct: false,
							      }, {
							       id: 48,
							       key: "C",
							       remark: " 可以确定被鉴定2人是否亲生关系",
							       correct: true,
							      }, {
							       id: 49,
							       key: "D",
							       remark: "可以确认被鉴定2人性别",
							       correct: true,
							      }],
							      type: "multiple",
							      type_name: "多选",
							    }
				],
				}
	},
	onShow() {
		// console.log(this.listArray,'123')
		this.listArray.forEach(v => {
				let a = []
				v.answers.forEach(item => a.push(item.key))
				this.ansArray.push(a)
		})
		console.log(this.ansArray, '123');
	}
	}
</script>

