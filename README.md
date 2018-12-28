# 3  
成员16301116 朱永锐  
    16301093 黄镇海  
 这里直接使用了VideoView，url是从网上找到的一个MP4类型的视频  
 private VideoView videoview1;  
    @Override  
    protected void onCreate(Bundle savedInstanceState) {  
        super.onCreate(savedInstanceState);  
        setContentView(R.layout.activity_video);  
        //本地的视频 需要在手机SD卡根目录添加一个Demo.mp4 视频  
        // String videoUrl1 = Environment.getExternalStorageDirectory().getPath()+"/Demo.mp4" ;  
        //网络视频  
        videoview1 = (VideoView) this.findViewById(R.id.videoView1);  
        //设置视频控制器  
        videoview1.setMediaController(new MediaController(this));  
        //播放完成回调  
        videoview1.setOnCompletionListener(new MyPlayerOnCompletionListener());  
        //设置视频路径  
        //videoView.setVideoURI(uri);  
        videoview1.setVideoPath("http://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4");  
        //开始播放视频  
        videoview1.start();  
    }  
    class MyPlayerOnCompletionListener implements MediaPlayer.OnCompletionListener {  
       @Override  
        public void onCompletion(MediaPlayer mp) {  
            Toast.makeText(VideoActivity.this, "播放完成了", Toast.LENGTH_SHORT).show();  
        }  
    }  
![Image text](https://github.com/16301116/3/blob/master/1.png)  
这是拨打电话的场景  
![Image text](https://github.com/16301116/3/blob/master/2.png)
