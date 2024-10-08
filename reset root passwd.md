Q15. Reset root user password and make it 'trootent'
select rescous 0
click to input=>keyboard=>select option=>clt+alt+del

select rescous o => press e for edit
fst line in the last write=> rd.break console=tty0
press f10

mount -o remount -rw /sysroot
chroot /sysroot
passwd root
touch /.autorelable

exit 
exit
