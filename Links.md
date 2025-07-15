---
tags:
  - COMP206
---
# Links


A symbolic (soft) link is:: a pointer to another file or directory. It acts as a shortcut.
<!--SR:!2025-02-21,82,230-->

Syntax to create symbolic links:
?
  ```bash
  ln -s target_link_name symlink_name
  ```
<!--SR:!2024-12-30,59,250-->

A hard link is:: a mirror copy of a file. Both the original file and hard link point to the same inode (data block) (only works for file even if the original file deleted).
<!--SR:!2024-12-10,20,150-->
  
Syntax to create hard links:
?
  ```bash
  ln target_link_name hardlink_name
  ```
<!--SR:!2024-12-19,52,250-->
