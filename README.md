# convert-an-image-into-ascii
import sys
from PIL import Image
image_path = sys.argv[0]
img = image.open("profile.jpg")
width,height = image.size
aspect_ratio = height/width
new_width = 120
new_height = aspect_ratio*new_width*0.55
img = img.resize((new_width,int(new_height)))
img=img..conert('L')
pixels=img.getdata()
chars = ["B","S","#","&","@","$","%","*","!",":","."]
new_pixels = [chars[pixel//25] for pixel in pixels]
pixels = ''.join (new_pixels)
new_pixels_count = len(new_pixels)
ascii_image = [new_pixels[index:index+newwidth] for index in range (0,new_pixels_count,new_width)]
ascii_image = "\n".join(ascii-image)
with open("ascii_image.txt",'w') as f:
f.write(ascii-image)
