<template>
    <div>
        <div class="header">
            <div>
                <text class="text_usrname">周卓潜</text>
                <text class="text_company">拓边/项目组长 </text>
                <text class="text_usr_exp">7年工作经验/本科/28岁 </text>
            </div>
            <image class="avatar" src="http://www.lgstatic.com/i/image2/M01/AC/4E/CgoB5lvxIMyAc6ZxAABPlqgpMDw351.png"></image>
        </div>
        <div class="block">
            <div class="sep_line"></div>
            <text class="block_title">自我描述</text>
            <div class="self_desc">
                <text class="self_desc_content">{{self_desc_content}}</text>
            </div>
        </div>

        <div class="block">
            <text class="block_title">工作经历</text>
            <list>
                <cell v-for="(num, i) in work_exps" :key="i">
                    <div class="list_panel">
                        <text class="work_exp_com">{{num['com']}}</text>
                        <text class="work_exp_title">{{num['title']}}</text>
                        <text class="work_exp_time">{{num['time']}}</text>
                        <text class="work_exp_dep">{{num['department']}}</text>
                        <text class="work_exp_content">{{num['desc']}}</text>
                    </div>
                </cell>
            </list>
        </div>

        <div class="block">
            <div class="sep_line_short"></div>
            <text class="block_title">项目经历</text>
            <list>
                <cell v-for="(num, i) in prj_exps" :key="i">
                    <div class="list_panel">
                        <text class="work_exp_com">{{num['com']}}</text>
                        <text class="work_exp_title">{{num['title']}}</text>
                        <text class="work_exp_content">{{num['desc']}}</text>
                    </div>
                </cell>
            </list>
        </div>

        <div class="block">
            <div class="sep_line_short"></div>
            <text class="block_title">教育经历</text>
            <div class="list_panel">
                <text class="work_exp_com">厦门大学嘉庚学院</text>
                <text class="work_exp_title">本科    计算机科学与技术</text>
                <text class="work_exp_content">2008-2012</text>
            </div>
        </div>
    </div>
</template>

<script>
  export default {
    data () {
      return {
        self_desc_content: '团队合作方面, 本人喜欢多沟通，以往工作养成了每日晨会的习惯, 时间控制在15分钟左右, 有需要的时候碰面交流比文档沟通更快捷, 尽量避免没必要的文档, 提高工作效率, 平时大家技术博客共享',
        work_exps: [
          {
            com: '拓边',
            title: '项目组长',
            time: '2013.09-至今',
            department: '研发部',
            desc: '1. 与上市公司石基信息合作开发西软酒店管理系统微信端酒店预订系统. 该项目主要包括客房预订模块, 酒店导航模块, 客服联系模块, 下单通知后台模块. 在这个项目里本人主要负责与西软的开发人员进行API对接, 同时本人负责后台逻辑(PHP)编写. 在项目管理方面, 团队严格执行按照技术API文档先行的原则, 制定一致的编码规则, 封装公有类, 提取常用函数等, 有效的提升了开发效率.\n' +
              '\n' +
              '2. 为对白茶舍开发web端在线商城.\n' +
              '\n' +
              '3. 为宁波樽肆红酒开发移动端hybrid框架双平台在线商城https://itunes.apple.com/us/app/z.selection/id996293119?l=zh&ls=1&mt=8该项目是一个标准的电商. 在本人主导下, 该项目采取了Hybrid技术解决方案, 让web端一次开发, 多平台运行, 将原有的开发时间缩小了50%, 同时本人承担了iOS客户端开发hybrid框架搭建工作. \n' +
              '\n' +
              '4. 为宁波中为星瓷砖拼花开发iPad 3D第一视角瓷砖掌上体验移动端产品.该项目是一个3D项目, 包含场景建模, 灯光渲染, 交互界面等. 本人主要负责管理整体项目进度, 与建模人员和设计人员对接工作, 并独立完成所有编码工作. 由于首次接手3D项目开发, 中途发生了一些卡壳的状况, 并在场景渲染中遇到诸多问题, 有惊无险, 最终圆满完成开发任务.\n' +
              '\n' +
              '5. 微信掌中宝(微信端一站式解决方案) http://wxzzb.com/\n' +
              '\n' +
              '6. 牛牛在线棋牌游戏(手游)\n' +
              '\n' +
              '7. 飞吧葫芦娃(2D手游)\n' +
              '\n' +
              '8. 大富翁(iOS端积分墙应用)\n' +
              '\n' +
              '9. 快点(iOS通知栏插件)\n' +
              '\n' +
              '10. 点金(Web端拖拽式量化投资工具)该项目是一个互联网金融项目, 主要是为了满足不会编程的人也可以做量化投资. 主要功能包含拖拽实现技术面条件选择, 运行回测, 回测结果包含净值曲线, 收益率, beta等, 并配以机器学习以傻瓜式优化策略, 对参数进一步改进. 该项目是本人一手提出并决定立项, 本人主要负责研究竞品, 编写机器学习算法, 后台运算逻辑, 回测模块, 生成自动化交易代码等.\n' +
              '\n' +
              '自我介绍:scrum开发坚定执行者.项目开发方面, 本人习惯于将一个项目分解为多个sprint, 每个阶段都是可用模型, 循环迭代, 最终成型, 这样的好处在于能够在快速开发的节奏中, 也能及时添加/移除功能, 并在随时有可用模型展示. 团队合作方面, 本人喜欢多沟通，以往工作养成了每日晨会的习惯, 时间控制在15分钟左右, 有需要的时候碰面交流比文档沟通更快捷, 尽量避免没必要的文档, 提高工作效率, 平时大家技术博客共享，两个星期左右的频率做一次code review等等。'
          },
          {
            com: '欣欣旅游',
            title: 'iOS开发工程师',
            time: '2013.01-2013.09',
            department: '研发部',
            desc: '开发欣欣旅游app，负责列表页，首页，旅游目的地页面\n' +
              '\n' +
              '在开发中我们在积极配合业务需求的同时，不断进行重构，抽离公用组件，提升app运行速度和持续集成方面做了诸多努力，满足了老板随时带着正在研发中的app外出开会的需求\n' +
              '\n' +
              '开发，欣旅通（欣欣同业）app负责通讯界面、个人主页的开发。\n' +
              '\n' +
              '开发舆情卫士. 该项目主要包括百度微博舆情后台抓取, 文本分析, 关键词设置, 移动端舆情扫描查看最新舆情等功能. 移动的开发工作由本人完成'
          },
          {
            com: 'RingCentral厦门研发中心',
            title: 'iOS自动化测试工程师',
            time: '2012.02-2012.07',
            department: '研发部',
            desc: '搭建Jenkins自动化测试框架, 做持续集成, 根据测试用例, 编写自动化测试代码，在与开发团队的配合中，我们发现开发团队不太喜欢给UI元素打标签，同时业务需求经常变更导致UI tree结构经常发生变化，这时候对于我们自动化团队的要求更高了，我们迎难而上，增加代码的鲁棒性，在一个个的sprint中发挥了重要的力量'
          }
        ],
        prj_exps: [
          {
            com: '欣欣旅游线路',
            title: '2013.02-2013.09',
            desc: '该项目是2C的旅游类电商项目, 是欣欣旅游的独特旅游线路产品. \n' +
              '包含了目的地定位, 旅游产品搜索, 旅游产品下单, \n' +
              '电话咨询, 旅游产品列表页, 详情页,联系客服, \n' +
              '付款, 用户评价等模块. \n' +
              '摸透了整个电商App开发的流程, 在开发过程中不断的重构和code review让我意识到开发不仅仅要满足业务需求, 同时为了整个项目的可维护性, 做出的工作一点都不比业务层面的工作量小\n' +
              '\n' +
              '\n' +
              '项目链接: https://itunes.apple.com/cn/app/id1312734679?ls=1&mt=8'
          },
          {
            com: '同业助手',
            title: '2013.02-2013.09',
            desc: '厦门欣欣旅游(上市公司腾邦国际子公司, 天使投资人蔡文胜)\n' +
              '\n' +
              '欣旅通（欣欣同业）app\n' +
              '\n' +
              '\n' +
              '\n' +
              '包含同业询价(IM)功能, 个人主页(交换名片等)社交功能, 同业信息交换板块(timeline)\n' +
              '\n' +
              '负责通讯界面、个人主页等功能开发\n' +
              '\n' +
              '项目链接: https://itunes.apple.com/cn/app/id642122211?ls=1&mt=8'
          },
          {
            com: '同业助手',
            title: '2012.02-2012.09',
            desc:'app store链接:\n' +
              '\n' +
              'https://itunes.apple.com/us/app/ringcentral-phone/id293305984?mt=8\n' +
              '\n' +
              '\n' +
              '\n' +
              '美国上市公司RingCentral的App\n' +
              '\n' +
              '这是一个IP电话云计算服务app, 主要是提供给中小企业工作沟通, 主要功能有sms, fax, IP云电话, voice mail等\n' +
              '\n' +
              '\n' +
              '\n' +
              '负责iOS自动化测试的框架搭建和代码编写'
          }
        ]
      }
    }
  }
</script>

<style scoped>

    .sep_line_short{
        margin-left: 50px;
        margin-right: 50px;
        height: 2px;
        background-color: #ccc;

    }
    .sep_line{
        margin-left: 0px;
        margin-right: 0px;
        height: 2px;
        background-color: #ccc;

    }
    .list_panel{
        margin-top: 80px;
        margin-left: 50px;
        margin-right: 50px;
    }
    .work_exp_content{
        margin-top: 25px;
        color: #666;
        font-size: 30px;
    }
    .work_exp_dep{
        margin-top: 50px;
        color: #000;
        font-size: 35px;
    }
    .work_exp_time{
        margin-top: 25px;
        color: #666;
        font-size: 30px;
    }
    .work_exp_title{
        margin-top: 25px;
        color: #666;
        font-size: 35px;
    }
    .work_exp_com{
        margin-top: 25px;
        color: #000;
        font-size: 40px;
    }
    .block{
        margin-top:25px;
        margin-bottom:60px;
    }
    .self_desc_content{
        margin-left: 25px;
        margin-top: 25px;
        margin-bottom: 25px;
        margin-right: 25px;
        color: #666;
        font-size: 30px;
    }
    .self_desc{
        margin-top: 35px;
        margin-left: 50px;
        margin-right: 50px;
        border-color: whitesmoke;
        border-width: 3px;
    }
    .block_title{
        margin-left: 50px;
        margin-top: 50px;
        color: #000000;
        font-size: 45px;
    }
    .header{
        flex-direction: row;
        margin-bottom: 50px;
    }
    .avatar {
        position: absolute;
        right: 50px;
        top: 50px;
        /*margin-right: 50px;*/
        /*margin-top: 50px;*/
        width: 212px;
        height: 212px;
        border-radius: 212px;
    }
    .text_usrname {
        margin-left: 50px;
        margin-top: 50px;
        color: #000000;
        font-size: 80px;
    }
    .text_company {
        margin-left: 50px;
        margin-top: 10px;
        color: #666666;
        font-size: 30px;
    }
    .text_usr_exp {
        margin-left: 50px;
        margin-top: 15px;
        color: #666666;
        font-size: 30px;
    }

</style>
