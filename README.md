from pathlib import path

import boto3
from mypy_boto3_rekognition.type_defs import (
    CelebrytyTypeDef, 
    recongnizecelebritiesresponseTypeDef,

)
from PIL import Imagem, ImagemDraw, ImageFont

Client = boto3.client("rekognition")

def get_path(file_name: str) -> str: 
    return str(path(__file__).parent / "images" / file_name)

def recognize_celebrities(photo: str) -> recongnizecelebritiesresponseTypeDef: 
    with open(photp, "rb") as image: 
        return cliente.recognize_celebrities(image={"bytes": image.read()})


def draw_boxes (image_path: str, output_path: str, face_details: list[celebrityTypeDef]):
    image = image.open(imagem_path)
    draw = imagemdraw.draw(image)
    font = imagemfont.trueType("ubuntu-R,ttF", 20)

    width,height = imagem.size
