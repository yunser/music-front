<template>
    <my-page title="首页">
        <div class="common-container container">
            <h1>APlayer</h1>
            <div id="player1" class="aplayer"></div>
        </div>
    </my-page>
</template>

<script>
    /* eslint-disable */
    // const MusicPlayer = require('../MusicPlayer')
    import MusicPlayer from '../MusicPlayer'

    export default {
        data () {
            return {
                page: {
                    menu: [
                        {
                            type: 'icon',
                            icon: 'help',
                            to: '/help'
                        }
                    ]
                }
            }
        },
        mounted() {
            let music = [
                {
                    title: '小幸运',
                    author: '田馥甄',
                    url: '/static/music/1.mp3',
                    pic: 'http://devtest.qiniudn.com/回レ！雪月花.jpg',
                    lrc: "/static/music/1.lrc"
                },
                {
                    title: 'あっちゅ～ま青春!',
                    author: '七森中☆ごらく部',
                    url: 'http://devtest.qiniudn.com/あっちゅ～ま青春!.mp3',
                    pic: 'http://devtest.qiniudn.com/あっちゅ～ま青春!.jpg',
                    lrc: "あっちゅ～ま青春!.lrc"
                },
                {
                    title: 'secret base~君がくれたもの~',
                    author: '茅野愛衣',
                    url: 'http://devtest.qiniudn.com/secret base~.mp3',
                    pic: 'http://devtest.qiniudn.com/secret base~.jpg',
                    lrc: "secret base~君がくれたもの~.lrc"
                }
            ];


            let player = new MusicPlayer({
                element: document.getElementById('player1'),
                narrow: false,
                autoplay: false,
                showlrc: 3,
                mutex: true,
                theme: '#e6d0b2',
                preload: 'metadata',
                mode: 'circulation',
                music: music
            });
        }
    }
</script>

<style scoped>
</style>
