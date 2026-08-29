# hello-world1
ที่เก็บข้อมูลนี้มีไว้สำหรับฝึกฝน GitHub Flow"
# 1. ต้องติดตั้งไลบรารีก่อน โดยพิมพ์คำสั่งนี้ใน Terminal:
# pip install moviepy

from moviepy.editor import VideoFileClip, concatenate_videoclips

# --- ขั้นตอนที่ 1: โหลดไฟล์วิดีโอ ---
clip1 = VideoFileClip("video1.mp4")
clip2 = VideoFileClip("video2.mp4")

# --- ขั้นตอนที่ 2: ตัดช่วงเวลา (Trimming) ---
# ตัดวิดีโอช่วงวินาทีที่ 0 ถึง 5
sub_clip1 = clip1.subclip(0, 5) 

# --- ขั้นตอนที่ 3: รวมคลิปเข้าด้วยกัน (Concatenation) ---
final_clip = concatenate_videoclips([sub_clip1, clip2])

# --- ขั้นตอนที่ 4: บันทึกวิดีโอที่ตัดต่อแล้ว ---
final_clip.write_videofile("output_edited.mp4")
