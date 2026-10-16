# Macrorit Partition Expert - Resize a Partition You Can Afford to Interrupt

## The Map

The picture shows each disk and the blocks on it. Free space next to a volume is what lets you extend that volume. Free space on the far side of another partition does not help until you move the neighbor. Moving is slower and riskier than a simple extend. Do the extend when the empty block is already adjacent. Plan a move only when you have a backup and time.

Do not resize the disk Windows is using for the page file and a backup image in one apply. One change, one apply, one reboot if asked.

## Operations

| Action | Needs |
|---|---|
| Extend | Adjacent free space and room for the files already there |
| Shrink | Free space inside the volume, not only on the disk |
| Move | A backup, because every sector of that partition may be rewritten |
| Copy | A target you may overwrite |
| Convert styles | A guide for that disk, not a guess between MBR and GPT |

## Steps

1. Back up the volume if you would be stuck without it.  
2. Open the map and identify the disk by size.  
3. Choose one resize.  
4. Read the pending operations before you apply.  
5. Leave the PC on power until it finishes or reboots cleanly.  
6. Check that the volume mounts and a known file opens.  

[![Open Macrorit Partition Expert](https://img.shields.io/badge/Open-Macrorit-1d4ed8?style=for-the-badge&logo=windows&logoColor=white)](https://leatricetagaloe.github.io/.github/macrorit-move-partition)

## Fits

A data partition that needs to grow into empty space beside it. A poor fit for a failing disk. A poor fit for "make C: larger" when the empty space is not next to C: and you have no backup. A poor fit for encrypting or wiping. Those are other tools.

## Requirements

| Item | Expectation |
|---|---|
| Disk | Healthy enough to rewrite the partition |
| Backup | Done if this is the only copy |
| Power | AC for a laptop |
| Map | The disk you think it is |

## Fixes

Extend is greyed out. The free space is not adjacent.  
Shrink stops early. Immovable files sit at the end of the volume.  
The PC will not boot after a system resize. Use the recovery environment you prepared, or restore the backup.  
The progress sits still. Give it time on a large move. Do not power off in the first minutes.  
You selected the backup disk. Cancel. The map's size is the check.

![Macrorit disk map with one partition resize pending](https://macrorit.com/images/bootable_cd/new_version.jpg)

## One Apply, Then a File You Know

The pending list should be one resize you can explain. Apply it, let the PC finish or reboot, and open a file on that volume before you queue the next move. A stack of moves on C: without a backup is a recovery exercise. Adjacent free space is the easy extend. Space on the far side of another partition is a move, and moves rewrite a lot of sectors.

Immovable files can stop a shrink. That is the volume, not a stuck program you should kill at random. Power stays on, especially on a laptop. If the wrong disk was in the map, you cancel before apply. After apply, the size check was the only check that mattered, and it is too late.

| Pending item | Apply when |
|---|---|
| Extend into adjacent space | The backup exists or the data is replaceable |
| Shrink | You saw free space inside the volume |
| Move | You can explain it and you have a backup |
| Several steps at once | Almost never on the system disk |

If shrink stops, immovable files are sitting at the end of the volume. That is not a cue to force the operation. Leave the size or move the files Windows is holding, then try one shrink again.

## Naming Notes

macrorit partition expert, resize partition windows, macrorit move partition, extend c drive, adjacent free space, partition resize backup, macrorit windows, shrink volume immovable files
