# download and install https://www.nodebox.net/download/
# for each segment: file > export movie > from 1 to 175
# (1) concatenate segments, (2) add music and (3) negate
# 
# // https://trac.ffmpeg.org/wiki/Concatenate#samecodec
# (1) ffmpeg -f concat -safe 0 -i mylist.txt -c copy output1.mp4
# // https://stackoverflow.com/questions/11779490/how-to-add-a-new-audio-not-mixing-into-a-video-using-ffmpeg
# (2) ffmpeg -i output1.mp4 -i "[108: Demodays 2013] 9-surprise.mp3" -codec copy -shortest output2.mp4
# // https://trac.ffmpeg.org/wiki/FilteringGuide
# // https://www.ffmpeg.org/ffmpeg-filters.html#negate
# (3) ffmpeg -i output2.mp4 -vf negate output3.mp4
# 
# mylist.txt:
file '[110: Freestyle Compo Griesbach] 1-Invitation.mp4'
file '[110: Freestyle Compo Griesbach] 2-Invitation.mp4'
file '[110: Freestyle Compo Griesbach] 3-Invitation.mp4'
file '[110: Freestyle Compo Griesbach] 4-Invitation.mp4'
file '[110: Freestyle Compo Griesbach] 5-Invitation.mp4'
