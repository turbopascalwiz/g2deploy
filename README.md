integration points

HOW TO USE:

  ./deploy.sh BUILD={PROFILE} WORK=ZPOOL/DATASET DEPLOY


  ./install.sh WORK=zfs://root@host:/ZPOOL/DATASET BOOT=zfs:///dev/sda:/srv/zfs/ZPOOL/DATASET_MNTPT

  ./mirror.sh ../config/[type].mirrors [PROFILE-releases.mirrors]

  ./update.sh WORK=[...]

  ./esync.sh // uses ../config/ESYNC/*.mirrors




issues / dependencies :

  install will assume the originating dataset's key and mount points, also install does not have a schema build system, where as multiple disks and custom properties cannot be asserted conveniently. 






portage/

  *infrastructure\
  distfiles       # install data\
  snapshots       # portage tree snapshots, daily or every other daily\
  repos           # repo portage tree, THE most up todate sync\
  releases        # sys releases repo, install medium / stage3\
  binpkgs         # binpkg repo
  
  *g2d\
  patchfiles      # specific config files (etc/...)\
  packages        # package and conf files, per profile, such as hardened, selinux, gnome, gnome/systemd\
  profiles        # configs for real/virtual machines, host/domain name dependent\
  kernels         # repo for current and depricated kernels


working on:

  btrfs+xfs+ext4 integration [ install.sh ]



needs:

  update function
  
  review install function
  further updates per f/s and schema added

  network adapter mapping