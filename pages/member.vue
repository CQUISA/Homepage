<template>
  <div class="content">
    <el-table :data="tableData" style="width: 100%" :show-overflow-tooltip="false">
      <el-table-column align="center" header-align="center" prop="avatar" width="80">
        <template slot-scope="scope">
          <el-avatar :src="scope.row.avatar"></el-avatar>
        </template>
      </el-table-column>
      <el-table-column align="center" prop="id" label="ID"></el-table-column>
      <el-table-column align="center" header-align="center" prop="grade" label="年级" width="100"></el-table-column>
      <el-table-column align="center" header-align="center" prop="desc" label="个人说明"></el-table-column>
      <el-table-column align="center" header-align="center" prop="mail" label="联络邮箱"></el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tableData: [{
        avatar: 'https://q1.qlogo.cn/g?b=qq&nk=954727918&s=160',
        id: 'v0id',
        grade: '2019级',
        desc: '副社长'
      }, {
        avatar: 'https://q1.qlogo.cn/g?b=qq&nk=2865859175&s=160',
        id: 'Yunen',
        grade: '2018级',
        desc: '前副社长 / Web安全菜狗 / 鹅厂',
        mail: 'admin@0x002.com'
      }, {
        avatar: 'https://q1.qlogo.cn/g?b=qq&nk=939646437&s=160',
        id: '正元',
        grade: '2018级',
        job: '前社长',
        desc: '前社长'
      }, {
        avatar: 'https://q1.qlogo.cn/g?b=qq&nk=864137698&s=160',
        id: '侯哥',
        grade: '2017级',
        desc: '密码带佬 / 中科院在读博士生',
        mail: 'houchengan@iie.ac.cn'
      }, {
        avatar: 'https://q1.qlogo.cn/g?b=qq&nk=965153603&s=160',
        id: '脐橙',
        grade: '2017级',
        desc: '前社长 / 深信服',
        mail: 'admin@lolpzili.com'
      }, {
        avatar: 'https://q1.qlogo.cn/g?b=qq&nk=1099718640&s=160',
        id: 'DYBOY',
        grade: '2016级',
        desc: 'Web安全 / 字节跳动 / 前端开发',
        mail: 'dyboy2017@qq.com'
      },{
        avatar: 'https://q1.qlogo.cn/g?b=qq&nk=876707908&s=160',
        id: 'Haochen',
        grade: '2016级',
        desc: '趋势科技 / 手机电脑Web前端后端都会写一点的开发',
        mail: 'jhc_98219@live.com'
      }, {
        avatar: 'https://q1.qlogo.cn/g?b=qq&nk=1109633841&s=160',
        id: 'Xx.',
        grade: '2016级',
        desc: '单位人员',
        mail: 'xhy147159@qq.com'
      }, {
        avatar: 'https://q1.qlogo.cn/g?b=qq&nk=545166605&s=160',
        id: 'Jason Yao',
        grade: '2016级',
        desc: '创始人 / 前副社长 / 系统安全 / 云安全 / 中科院在读博士生',
        mail: '545166605@qq.com'
      }, {
        avatar: 'https://q1.qlogo.cn/g?b=qq&nk=847412245&s=160',
        id: '沧流',
        grade: '2016级',
        desc: '创始人 / 前社长 / 腾讯科恩实验室 / 恶意代码分析',
        mail: 'unkn0wn9@outlook.com'
      }, {
        avatar: 'https://q1.qlogo.cn/g?b=qq&nk=916191052&s=160',
        id: 'YUE',
        grade: '2014级',
        desc: '创始人 / 前社长 / 字节跳动 / 抖音产品经理',
        mail: 'kcahyl@foxmail.com'
      }
      ]
    }
  }
}
</script>
