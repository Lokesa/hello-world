data segment
  mesage db "hello world!",0dh,0ah,24h
data ends
code segement
  assume cs:code,ds:data
start:mov ax,data
  mov ds,ax
  lea dx,mesage
  mov ah,4ch
  int 21h
code ends
     ends start
