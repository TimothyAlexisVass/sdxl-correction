from PIL import Image
import os

def convert_png_to_jpg(png_path, jpg_path):
    im = Image.open(png_path)
    rgb_im = im.convert('RGB')
    rgb_im.save(jpg_path)
    os.remove(png_path)
    print(f"Converted: {png_path} to {jpg_path}")

def convert_folder(folder_path):
    for filename in os.listdir(folder_path):
        if filename.endswith(".png"):
            png_path = os.path.join(folder_path, filename)
            jpg_path = os.path.join(folder_path, os.path.splitext(filename)[0] + ".jpg")
            convert_png_to_jpg(png_path, jpg_path)

if __name__ == "__main__":
    folder_path = "./"
    convert_folder(folder_path)
