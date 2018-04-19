<template>
  <div class="content">
    产品
    <el-row>
	  <el-button>默认按钮</el-button>
	  <el-button type="primary">主要按钮</el-button>
	  <el-button type="success">成功按钮</el-button>
	  <el-button type="info">信息按钮</el-button>
	  <el-button type="warning">警告按钮</el-button>
	  <el-button type="danger">危险按钮</el-button>
	</el-row>

	<el-row>
	  <el-button plain>朴素按钮</el-button>
	  <el-button type="primary" plain>主要按钮</el-button>
	  <el-button type="success" plain>成功按钮</el-button>
	  <el-button type="info" plain>信息按钮</el-button>
	  <el-button type="warning" plain>警告按钮</el-button>
	  <el-button type="danger" plain>危险按钮</el-button>
	</el-row>

	<el-row>
	  <el-button round>圆角按钮</el-button>
	  <el-button type="primary" round>主要按钮</el-button>
	  <el-button type="success" round>成功按钮</el-button>
	  <el-button type="info" round>信息按钮</el-button>
	  <el-button type="warning" round>警告按钮</el-button>
	  <el-button type="danger" round>危险按钮</el-button>
	</el-row>

	<el-row>
	  <el-button icon="el-icon-search" circle></el-button>
	  <el-button type="primary" icon="el-icon-edit" circle></el-button>
	  <el-button type="success" icon="el-icon-check" circle></el-button>
	  <el-button type="info" icon="el-icon-message" circle></el-button>
	  <el-button type="warning" icon="el-icon-star-off" circle></el-button>
	  <el-button type="danger" icon="el-icon-delete" circle></el-button>
	</el-row>
	<el-container style="height:500px;border:1px solid #eee">
		<el-aside width="200px" style="background-color:rgba(238,241,246)">
			<el-menu :default-openeds="['1','3']">
				<el-submenu index="1">
					<template slot="title"><i class="el-icon-message">导航一</i></template>
					<el-menu-item-group>
						<template slot="title">分组一</template>
						<el-menu-item index="1-1">选项一</el-menu-item>
						<el-menu-item index="1-2">选项二</el-menu-item>
					</el-menu-item-group>
					<el-menu-item-group title="分组2">
						<el-menu-item index="1-3">选项三</el-menu-item>
					</el-menu-item-group>
					<el-submenu index="1-4">
						<template slot="title">选项4</template>
						<el-menu-item index="1-4-1">选项4-1</el-menu-item>
					</el-submenu>
				</el-submenu>
				<el-submenu index="2">
					<template slot="title"><i class="el-icon-menu">导航2</i></template>
					<el-menu-item-group>
						<template slot="title">分组一</template>
						<el-menu-item index="2-1">选项1</el-menu-item>
						<el-menu-item index="2-2">选项2</el-menu-item>
					</el-menu-item-group>
				</el-submenu>
			</el-menu>
		</el-aside>
		<el-container>
			<el-header style="text-align:right;font-size:12px">
				<el-dropdown>
					<i class="el-icon-setting" style="marign-right:15px"></i>
					<el-dropdown-menu slot="dropdown">
						<el-dropdown-item>查看</el-dropdown-item>
						<el-dropdown-item>新增</el-dropdown-item>
						<el-dropdown-item>删除</el-dropdown-item>
					</el-dropdown-menu>
				</el-dropdown>
				<span>王小虎</span>
			</el-header>
			<el-main>
				<el-table :data="tableData">
					<el-table-column prop="data" label="日期" width="140"></el-table-column>
					<el-table-column prop="name" label="姓名" width="120"></el-table-column>
					<el-table-column prop="address" label="地址"></el-table-column>
				</el-table>
			</el-main>
		</el-container>
	</el-container>
	<el-container>
		<el-header>Header</el-header>
		<el-container>
			<el-aside width="200px">Aside</el-aside>
			<el-container>
				<el-main>Main</el-main>
				<el-footer>Footer</el-footer>
			</el-container>
		</el-container>
	</el-container>
  </div>
  
</template>
<script>
export default {
	name: 'Product',
	data(){
		const item = {
			data:'2016-04-12',
			name:'王小虎',
			address:'上海市普陀区金沙江路 1518 弄'
		};
		return {
			tableData:Array(20).fill(item)
		}
	},
	methods: {
		goBack(){
			console.log(this.$router.go(-1));
		}
	}
}
</script>
<style >
  .el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }
  
  .el-aside {
    background-color: #D3DCE6;
    color: #333;
    text-align: center;
    line-height: 200px;
  }
  
  .el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    line-height: 160px;
  }
  .el-header {
    background-color: #B3C0D1;
    color: #333;
    line-height: 60px;
  }
  
  .el-aside {
    color: #333;
  }
</style>
