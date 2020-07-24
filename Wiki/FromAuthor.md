# 前言

BiliRec其实是我闲暇之余的一个构想，然后趁着疫情期间闲着就着手开始写了。

我自己写代码的习惯说实话挺差的所以这玩意儿的可读性应该不咋地，献丑了。

BiliRec的工作模式说白了就是用Streamlink（一个基于Python的开源项目）去监测直播推流并且读取视频流，然后由FFMPEG进行编码和保存，一个非常简单粗暴的方式。

我在2018年暑假期间就写过一个自动录播的脚本，当然那个脚本问题也挺大的。这次主要就是改了一些小地方的问题然后做了Linux和Windows的适配。最近也在学习Django的项目开发所以就给加入了一个可视化的Web端监控模块，这个模块目前还在开发中并不完善，姑且算是能拿出来看看的程度，后续还会进行开发。

Streamlink也好，FFMPEG也好，对于新手来说着实不太友好，特别是FFMPEG的API过于晦涩难懂，最后我还是放弃了调用API直接暴力`os.system`。

这个项目仍有很多问题，我调试的时候并没有进行多方面的测试只是保证它能正常运行而已。如果在使用过程中遇到问题还请多多反馈，感谢支持。

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/gitalk@1/dist/gitalk.css">

<script src="https://cdn.jsdelivr.net/npm/gitalk@1/dist/gitalk.min.js"></script>

<div id="gitalk-container"></div>

<script>
    const gitalk = new Gitalk({
        clientID: "a9f7d3f091928b45e225",
        clientSecret: "af98a2e872ffd57b4443842cd200d5acf50d7f7d",
        repo: "BiliRec",
        owner: "Dreammer12138",
        admin: ['Dreammer12138'],
        id: location.pathname
    });
    gitalk.render('gitalk-container');
</script>