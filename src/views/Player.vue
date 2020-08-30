<template>
    <my-page title="播放器">
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
            // https://www.80wp.com/file/106304.html
            let music = [
                {
                    title: '小幸运',
                    author: '田馥甄',
                    url: '/static/music/1.mp3',
                    pic: 'http://devtest.qiniudn.com/回レ！雪月花.jpg',
                    lrc: "/static/music/1.lrc"
                },
                {
                    title: '少年',
                    author: '梦然',
                    url: '/static/music/2.mp3',
                    pic: 'http://devtest.qiniudn.com/あっちゅ～ま青春!.jpg',
                    lrc: "/static/music/2.lrc"
                },
                {
                    title: '童话镇',
                    author: '陈一发儿',
                    url: '/static/music/3.mp3',
                    pic: 'http://devtest.qiniudn.com/secret base~.jpg',
                    lrc: "/static/music/3.lrc"
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
