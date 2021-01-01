 .model small
.stack 100h
.data
Var db 5 dup(?)
.code
Main proc
	Mov ax,@data
	Mov ds,ax
             Mov ah,1
	Int 21h
	Mov var[si],al
 Mov ah,1
	Int 21h
	Mov var[si+1],al
             Mov ah,1
	Int 21h
	Mov var1[si+2],al
             Mov ah,1
	Int 21h
	Mov var1[si+3],al
	 Mov ah,1
	Int 21h
	Mov var1[si+4],al

Mov dx,offset var
Mov cl,[si+2]
Mov bl,[si+4]
Add cl,bl
Mov dl,cl
Sub dl,48
mov ah,2
int 21h
mov ah, 4ch
int 21h	
main endp
end main
