<template>
	<div class="container">
		<div style="min-height: calc(100vh - 80px);">
			<el-row>
				<el-col :span="24" style="text-align: center; margin-top: 80px;">
					<el-image style="max-width: 350px;" src="/images/logo.jpg"></el-image>
				</el-col>
				<el-col :span="24" style="text-align: center; margin-top: 30px;">
					<div class="breadcrumd">
						<el-breadcrumb separator="/">
							<el-breadcrumb-item :to="{ path: '/' }">社团介绍</el-breadcrumb-item>
							<el-breadcrumb-item :to="{ path: '/intro' }">研究方向</el-breadcrumb-item>
							<el-breadcrumb-item :to="{ path: '/member' }">社团成员</el-breadcrumb-item>
							<el-breadcrumb-item :to="{ path: '/glory' }"><strong style="cursor: pointer;">社团荣誉</strong></el-breadcrumb-item>
						</el-breadcrumb>
					</div>
				</el-col>
			</el-row>
			<el-row justify="center" type="flex">
				<el-col :md="12" :lg="8" :sm="18" :xs="22">
					<nuxt />
				</el-col>
			</el-row>
		</div>

		<div class="footer">
			<div class="footer-icon">
				<el-popover placement="top" width="100" trigger="click">
					<el-image style="max-width: 350px;" src="/images/weixin.png"></el-image>
					<el-button type="text" slot="reference">
						<svg class="icon" aria-hidden="true">
							<use xlink:href="#icon-weixin"></use>
						</svg>
					</el-button>
				</el-popover>
				<el-popover placement="top" width="100" trigger="click">
					<el-image style="max-width: 350px;" src="/images/weibo.png"></el-image>
					<el-button type="text" slot="reference">
						<svg class="icon" aria-hidden="true">
							<use xlink:href="#icon-weibo"></use>
						</svg>
					</el-button>
				</el-popover>
				<el-popover placement="top" width="100" trigger="click">
					<el-image style="max-width: 350px;" src="/images/qqgroup.png"></el-image>
					<el-button type="text" slot="reference">
						<svg class="icon" aria-hidden="true">
							<use xlink:href="#icon-QQ"></use>
						</svg>
					</el-button>
				</el-popover>
			</div>
			<div class="footer-info">
				Contact Email: <a href="mailto:public@cquisa.com" target="_blank">public@cquisa.com</a>
			</div>
			<div class="footer-copyright">
				<span>Copyright © 2017-{{(new Date()).getFullYear()}} CQUISA. All rights reserved.</span>
			</div>
		</div>

		<style>
			.el-breadcrumb .el-breadcrumb__item:nth-child({{ url_list.indexOf($route.path)+1 }}) .el-breadcrumb__inner {
				color: #F76262 !important;
			}
		</style>

	</div>
</template>

<script>
	import '~/assets/iconfont/iconfont.js'

	export default {
		data() {
			return {
				url_list: ['/', '/intro', '/member', '/glory']
			}
		},
		mounted() {}
	}
</script>

<style>
	.el-breadcrumb .el-breadcrumb__item:nth-child(4) .el-breadcrumb__inner {
		color: #303133;
	}

	.footer-icon .el-button--text {
		color: initial !important;
	}


	.icon {
		width: 1em;
		height: 1em;
		vertical-align: -0.15em;
		fill: currentColor;
		overflow: hidden;
	}

	.content {
		margin-top: 60px;
		margin-bottom: 40px;
	}

	.breadcrumd {
		display: inline-block;
		margin: 0 auto;
		padding: 10px;
	}

	.breadcrumd span {
		font-size: 16px;
	}

	.footer-copyright span,
	.footer-icon,
	.footer-info{
		display: block;
		text-align: center;
    font-size: 14px;
	}

	.footer-icon svg {
		font-size: 30px;
	}

	.footer-icon .el-button {
		padding: 0px;
	}

	.footer-info a:link {
		color: #000000;
		text-decoration: none;
	}

	.footer-info a:visited {
		color: #000000;
		text-decoration: none;
	}

	.footer-info a:hover {
		color: #999999;
		text-decoration: underline;
	}

  .footer {
    margin-bottom: 10px;
  }

	body {
		margin: 0px;
	}
</style>
