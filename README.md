Download Link: https://assignmentchef.com/product/solved-cs314-lab-6
<br>
<span class="kksr-muted">Rate this product</span>

In this assignment, /home is a separate file system of type mfs. With this trace the working on the mfs file system, only for the file system mounted at /home has to be taken care of.

1.1 File Created

For the file creation, the file open.c at location: minix/servers/vfs/open.c was changed. It was used in function common open().

printf(“file created: %llu
”, vp-&gt;v_inode_nr);Figure 1 shows the implementation in Minix. A simple file named newFile was created

using touch newFile. 1.2 File Read

For the file read, the file read.c at location: minix/servers/vfs/read.c was changed. It was used in function read write().

<pre>printf("file read: %llu; nbytes = %zu; offset = %llu
", vp-&gt;v_inode_nr,size, f-&gt;filp_pos);</pre>

Figure 2 &amp; 3 shows the implementation in Minix. In order to read the file, cat newFile was used after some strings were written in file using Nano.

1.3 File Write

For the file write, the file read.c at location: minix/servers/vfs/read.c was changed. It was used in function read write().

<pre>printf("file written: %llu; nbytes = %zu; offset = %llu
", vp-&gt;v_inode_nr,size, f-&gt;filp_pos);</pre>

Figure 4 shows the implementation for the file write case. Using, echo “Writing new Line” &gt; newFile to write into the file.

1

Figure 1: File Created

Figure 2: Write using Nano 2

Figure 3: File Read

Figure 4: File Write 3

1.4 File Deleted

Figure 5: File Delete

For the file delete, the file link.c at location: minix/servers/vfs/link.c was changed. It was used in function do unlink().

<pre>    printf("file deleted: %llu
", vp-&gt;v_inode_nr);</pre>

Figure 5 shows the implementation for the file delete case. In order to delete the file, rm newFile was used.