####composing videos#####

video_index=0
cap=cv2.VideoCapture(video[srt_time[video_index]])
width = int(cap.get(cv2.CAP_PROP_FRAME_WIDTH))
height = int(cap.get(cv2.CAP_PROP_FRAME_HEIGHT))
fps = cap.get(cv2.CAP_PROP_FPS)
count=cap.get(cv2.CAP_PROP_FRAME_COUNT)
fourcc = cv2.VideoWriter_fourcc(*'DIVX')
out = cv2.VideoWriter("Output.avi", fourcc, fps, (width, height), True)
while(cap.isOpened()):
    ret,frame=cap.read()
    if frame is None:
        print "end of video " + str(video_index) + " .. next one now"
        video_index += 1
        if video_index >= len(videoList):
            break
        cap = cv2.VideoCapture(video[srt_time[video_index]])
        ret, frame = cap.read()
    out.write(frame)


####using ffmpeg to merge two videos#####


ffmpeg -i left.mp4 -i right.mp4 -filter_complex \
"[0:v][1:v]hstack=inputs=2[v]; \
 [0:a][1:a]amerge[a]" \
-map "[v]" -map "[a]" -ac 2 output.mp4


####using ffmpeg to merge two videos 2#####


ffmpeg \
  -i input1.mp4 \
  -i input2.mp4 \
  -filter_complex '[0:v]pad=iw*2:ih[int];[int][1:v]overlay=W/2:0[vid]' \
  -map [vid] \
  -c:v libx264 \
  -crf 23 \
  -preset veryfast \
  output.mp4



################1################



from youtube_search_and_download import YouTubeHandler
search_key = 'chinese top ktv' #keywords
yy = YouTubeHandler(search_key)
yy.download_as_audio =1 # 1- download as audio format, 0 - download as video
yy.set_num_playlist_to_extract(5) # number of playlist to download
####composing videos#####

video_index=0
cap=cv2.VideoCapture(video[srt_time[video_index]])
width = int(cap.get(cv2.CAP_PROP_FRAME_WIDTH))
height = int(cap.get(cv2.CAP_PROP_FRAME_HEIGHT))
fps = cap.get(cv2.CAP_PROP_FPS)
count=cap.get(cv2.CAP_PROP_FRAME_COUNT)
fourcc = cv2.VideoWriter_fourcc(*'DIVX')
out = cv2.VideoWriter("Output.avi", fourcc, fps, (width, height), True)
while(cap.isOpened()):
    ret,frame=cap.read()
    if frame is None:
        print "end of video " + str(video_index) + " .. next one now"
        video_index += 1
        if video_index >= len(videoList):
            break
        cap = cv2.VideoCapture(video[srt_time[video_index]])
        ret, frame = cap.read()
    out.write(frame)


####using ffmpeg to merge two videos#####


ffmpeg -i left.mp4 -i right.mp4 -filter_complex \
"[0:v][1:v]hstack=inputs=2[v]; \
 [0:a][1:a]amerge[a]" \
-map "[v]" -map "[a]" -ac 2 output.mp4


####using ffmpeg to merge two videos 2#####


ffmpeg \
  -i input1.mp4 \
  -i input2.mp4 \
  -filter_complex '[0:v]pad=iw*2:ih[int];[int][1:v]overlay=W/2:0[vid]' \
  -map [vid] \
  -c:v libx264 \
  -crf 23 \
  -preset veryfast \
  output.mp4



################1################



from youtube_search_and_download import YouTubeHandler
search_key = 'chinese top ktv' #keywords
yy = YouTubeHandler(search_key)
yy.download_as_audio =1 # 1- download as audio format, 0 - download as video
yy.set_num_playlist_to_extract(5) # number of playlist to download
