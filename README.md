https://dbeaver.io/download/

<pre>
docker plugin install vieux/sshfs
docker plugin install --grant-all-permissions vieux/sshfs

docker plugin ls

docker volume create --driver vieux/sshfs \
       -o sshcmd=ateam@redash.feg.cn:/home/ateam \
       -o password=123456  \
       sshvolume

docker run --rm -it -v sshvolume:/data nginx ls /data
</pre>
