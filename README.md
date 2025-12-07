<!文档类型html >
<超文本标记语言语言=“zh-CN”>
<头>
  <自指的字符集=“UTF八号” />
  <自指的名字="视窗" 内容=宽度=设备宽度，初始比例=1.0/>
  <标题>纯净股筛选器</标题>
  <风格>
身体{
      字体系列: -苹果系统, BlinkMacSystemFont, " Segoe用户界面", 机器人, 无衬线字体;
      背景:# f8f 9 fa；
      边缘: 0;
      填料: 20像素;
    }
。容器{
      最大宽度: 800像素;
      边缘: 0 汽车;
      背景: 白色;
      边框半径: 12像素;
箱形阴影: 0 2像素 10像素rgba(0，0，0，0.05)；
      填料: 24像素;
    }
h1 {
文本对齐:居中；
颜色:# 2c3e50
边距-顶部:0；
    }
。desc {
背景:# e8f 4 ff；
填充:12px
边框半径:8px
边距-底部:20px
字体大小:14px
颜色:# 2980b9
    }
#库存清单{
显示:网格；
差距:12px
    }
。库存项目{
显示器:flex
填充:12px
背景:# fff
边框:1px纯色# eee
边框半径:8px
box-shadow: 0 1px 3px rgba(0，0，0，0.05)；
    }
。代码{
宽度:100px
字体粗细:粗体；
颜色:# e74c3c
    }
  </风格>
</头>
<身体>
  <差异班级="集装箱">
    <氕>✨ 纯净股筛选器</氕>
    <差异班级=《desc》>
自动筛选「无任何主流机构持仓」的A股：<英国铁路公司>
排除公募基金、社保、保险、券商、QFII、养老金、证金/汇金等。
    </差异>
    <差异身份证明（identification）="库存清单">
      <p 风格="文本对齐:center;color:#999;">正在加载最新数据...</p>
    </div>
  </div>

  <script>
    // === 配置你的腾讯文档ID ===
    const DOC_ID = "DVGZXT0dvUUhoT1ps"; // ← 这就是你刚才的文档ID！

    const API_URL = `https://docs.qq.com/dop-api/opendoc?outformat=1&id=${DOC_ID}&noCache=${Date.now()}`;

    fetch(API_URL)
      .then(res => res.json())
      .then(data => {
        if (data.code !== 0) throw new Error("文档读取失败");

        const records = data.data.records || [];
        常数 股票 = records.地图(排 => ({
          密码:行'',
          名字:行'—'
        })).过滤器(s => s.code.trim());

        渲染股票(股票);
      })
      .捕捉(犯罪 => {
控制台。错误("加载失败:"，呃);
文件。getElementById(“stocklist”).innerHTML = 
          < p style = "文本对齐:居中；颜色:# e74c3c ">⚠️ 数据加载失败,请稍后重试<< p style = " text-align:center；颜色:# e74c3c">⚠️ 数据加载失败,请稍后重试</p > '
      });

    功能 渲染股票(股票) {
      常数 平线脚=文档。getElementById('库存清单');
      如果 (股票。长度 === 0) {
利斯托尔。innerhtml = < p style = "文本对齐:居中；颜色:# 999;">暂无符合条件的股票；innerHTML = < p style = "文本对齐：居中；颜色:# 999;">暂无符合条件的股票</p > ';
返回；
      }
listel . innerhtml = stocks . 地图(stock = >innerHTML = stocks.地图(股票 => 
        `< div class="stock-item " >
< span class="code " >${stock.密码}</span >
< span >${stock.名字}</span >
</div > `
      ).加入('');
    }
  </脚本>
</</body >>
</</html >>
