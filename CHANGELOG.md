CHANGELOG
=========

1.2.7 (Mar 6, 2015)
====================

* Improvements
    * [#320](https://github.com/leo-project/leofs/issues/320) ``leo_mq`` Can take too much time to get started consuming messages in a MQ

* Fixed Bugs
    * [#313](https://github.com/leo-project/leofs/issues/313) ``leo_watchdog`` Watchdog downed every an hour
    * [#315](https://github.com/leo-project/leofs/issues/315) ``leo_redundant_manager`` Inconsistent storage node status
    * [#317](https://github.com/leo-project/leofs/issues/317) ``leo_redundant_manager`` Calling leo_manager_api:get_members_of_all_versions get timeout on leo_gateway
    * [#319](https://github.com/leo-project/leofs/issues/319) ``leo_gateway`` List Objects with ``next-marker`` could NOT work when using ``s3cmd`` as a client
    * [#322](https://github.com/leo-project/leofs/issues/322) ``leo_cache`` Set wrong value to a disk cache capacity
    * [#323](https://github.com/leo-project/leofs/issues/323) ``leo_dcerl`` LeoFS's gateway do not response or return HTTP error code 5xx

* Used libraries
    * leo project
        * [leo_backend-db v1.1.5](https://github.com/leo-project/leo_backend_db/releases/tag/1.1.5)
        * [leo_cache v0.6.3](https://github.com/leo-project/leo_cache/releases/tag/0.6.3)
        * [leo_commons v1.1.1](https://github.com/leo-project/leo_commons/releases/tag/1.1.1)
        * [leo_dcerl v0.2.12](https://github.com/leo-project/leo_dcerl/releases/tag/0.2.12)
        * [leo_logger v1.1.5](https://github.com/leo-project/leo_logger/releases/tag/1.1.5)
        * [leo_mcerl v0.4.1](https://github.com/leo-project/leo_mcerl/releases/tag/0.4.1)
        * [leo_mq v1.3.4](https://github.com/leo-project/leo_mq/releases/tag/1.3.4)
        * [leo_object_storage v1.2.4](https://github.com/leo-project/leo_object_storage/releases/tag/1.2.4)
        * [leo_ordning_reda v0.10.10](https://github.com/leo-project/leo_ordning_reda/releases/tag/0.10.10)
        * [leo_redundant_manager 1.9.8](https://github.com/leo-project/leo_redundant_manager/releases/tag/1.9.8)
        * [leo_rpc v0.10.0](https://github.com/leo-project/leo_rpc/releases/tag/0.10.0)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod/releases/tag/0.6.2)
        * [leo_s3_libs v1.1.6](https://github.com/leo-project/leo_s3_libs/releases/tag/1.1.6)
        * [leo_statistics v1.1.0](https://github.com/leo-project/leo_statistics/releases/tag/1.1.0)
        * [leo_watchdog v0.6.3](https://github.com/leo-project/leo_watchdog/releases/tag/0.6.3)
        * [savanna_agent v0.4.5](https://github.com/leo-project/savanna_agentreleases/tag/0.4.5)
        * [savanna_commons v0.8.7](https://github.com/leo-project/savanna_commons/releases/tag/0.8.7)
        * [erpcgen v0.2.3](https://github.com/leo-project/erpcgen/releases/tag/0.2.3)
        * [nfs_rpc_server v0.2.2](https://github.com/leo-project/nfs_rpc_server/releases/tag/0.2.2)
        * [leo_gateway v1.2.7](https://github.com/leo-project/leo_gateway/releases/tag/1.2.7)
        * [leo_manager v1.2.7](https://github.com/leo-project/leo_manager/releases/tag/1.2.7)
        * [leo_storage v1.2.7](https://github.com/leo-project/leo_storage/releases/tag/1.2.7)
    * others
        * [bitcask v1.7.1](https://github.com/leo-project/bitcask/releases/tag/1.7.1)
        * [cowboy v1.0.0](https://github.com/extend/cowboy/releases/tag/1.0.0)
        * [cowlib v1.0.0](https://github.com/extend/cowboy/releases/tag/1.0.0)
        * [elarm v0.3.0](https://github.com/leo-project/elarm/releases/tag/0.3.0)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb/releases/tag/1.4.10)
        * [folsom v0.8.1](https://github.com/boundary/folsom/releases/tag/0.8.1)
        * [jiffy v0.13.3](https://github.com/davisp/jiffy/releases/tag/0.13.3)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4/releases/tag/0.2.2) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)
        * [recon v0.8.5](https://github.com/ferd/recon/releases/tag/2.2.1)


1.2.6 (Feb 20, 2015)
====================

* Improvements
    * [#296](https://github.com/leo-project/leofs/issues/296) ``leo_commons`` Replace leo_hashtable with Erlang built-in function
    * [#305](https://github.com/leo-project/leofs/issues/305) ``leo_statistics`` some system metrics should be added for more reliability
* Fixed Bugs
    * [#307](https://github.com/leo-project/leofs/issues/307) ``leo_storage`` Could not respond not existed object immediately (LeoFS v1.2.5's bug)
        * LeoFS Gateway was timeout because LeoFS Storage could not respond not existed object immediately.
And also, load of a primary of storage-node became high by this issue.
        * We took measure for this situation we implemented [leofs_test2](https://github.com/leo-project/leofs_test2) which is an integration test tool.
    * [#308](https://github.com/leo-project/leofs/issues/308) ``leo_storage`` ``leo_gateway`` Could not synchronize 'suspend' status at each gateway and storage nodes
    * [#309](https://github.com/leo-project/leofs/issues/309) ``leo_redundant_manager`` ``leo_manager`` Ring status to be synced between mnesia and worker state
    * [#310](https://github.com/leo-project/leofs/issues/310) ``leo_gateway`` Delete request might consume CPU resource more than necessary
    * [#311](https://github.com/leo-project/leofs/issues/311) ``leo_storage`` Could NOT respond an object when facing the inconsistent object
* Used libraries
    * leo project
        * [leo_backend-db v1.1.4](https://github.com/leo-project/leo_backend_db/releases/tag/1.1.4)
        * [leo_cache v0.6.0](https://github.com/leo-project/leo_cache/releases/tag/0.6.0)
        * [leo_commons v1.1.0](https://github.com/leo-project/leo_commons/releases/tag/1.1.0)
        * [leo_dcerl v0.2.11](https://github.com/leo-project/leo_dcerl/releases/tag/0.2.11)
        * [leo_logger v1.1.4](https://github.com/leo-project/leo_logger/releases/tag/1.1.4)
        * [leo_mcerl v0.4.1](https://github.com/leo-project/leo_mcerl/releases/tag/0.4.1)
        * [leo_mq v1.3.3](https://github.com/leo-project/leo_mq/releases/tag/1.3.3)
        * [leo_object_storage v1.2.3](https://github.com/leo-project/leo_object_storage/releases/tag/1.2.3)
        * [leo_ordning_reda v0.10.9](https://github.com/leo-project/leo_ordning_reda/releases/tag/0.10.9)
        * [leo_redundant_manager 1.9.7](https://github.com/leo-project/leo_redundant_manager/releases/tag/1.9.7)
        * [leo_rpc v0.8.10](https://github.com/leo-project/leo_rpc/releases/tag/0.8.10)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod/releases/tag/0.6.2)
        * [leo_s3_libs v1.1.5](https://github.com/leo-project/leo_s3_libs/releases/tag/1.1.5)
        * [leo_statistics v1.0.9](https://github.com/leo-project/leo_statistics/releases/tag/1.0.9)
        * [leo_watchdog v0.6.2](https://github.com/leo-project/leo_watchdog/releases/tag/0.6.2)
        * [savanna_agent v0.4.4](https://github.com/leo-project/savanna_agentreleases/tag/0.4.4)
        * [savanna_commons v0.8.6](https://github.com/leo-project/savanna_commons/releases/tag/0.8.6)
        * [erpcgen v0.2.3](https://github.com/leo-project/erpcgen/releases/tag/0.2.3)
        * [nfs_rpc_server v0.2.2](https://github.com/leo-project/nfs_rpc_server/releases/tag/0.2.2)
        * [leo_gateway v1.2.6](https://github.com/leo-project/leo_gateway/releases/tag/1.2.6)
        * [leo_manager v1.2.6](https://github.com/leo-project/leo_manager/releases/tag/1.2.6)
        * [leo_storage v1.2.6](https://github.com/leo-project/leo_storage/releases/tag/1.2.6)
    * others
        * [bitcask v1.7.1](https://github.com/leo-project/bitcask/releases/tag/1.7.1)
        * [cowboy v1.0.0](https://github.com/extend/cowboy/releases/tag/1.0.0)
        * [cowlib v1.0.0](https://github.com/extend/cowboy/releases/tag/1.0.0)
        * [elarm v0.3.0](https://github.com/leo-project/elarm/releases/tag/0.3.0)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb/releases/tag/1.4.10)
        * [folsom v0.8.1](https://github.com/boundary/folsom/releases/tag/0.8.1)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy/releases/tag/0.2.2)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4/releases/tag/0.2.2) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)
        * [recon v0.8.5](https://github.com/ferd/recon/releases/tag/2.2.1)


1.2.5 (Jan 29, 2015)
====================

* New Features
    * Started to provide LeoFS integration test tool - [leofs_test](https://github.com/leo-project/leofs_test2)
        * We're able to easily check LeoFS with it whether latest LeoFS has issues or not before getting installed LeoFS in your dev/staging/production environment(s).
* Fixed Bugs
    * [#299](https://github.com/leo-project/leofs/issues/299) ``leo_redundant_manager`` Inconsistent ring of a resumed storage-node which is timing issue
    * [#301](https://github.com/leo-project/leofs/issues/301) ``leo_storage`` Replication messages could be lost in some edge cases
    * ``leo_storage`` Fix the read-and-repair mechanism. Some inconsistent data could not recover with it.
* Used libraries
    * leo project
        * [leo_backend-db v1.1.4](https://github.com/leo-project/leo_backend_db/releases/tag/1.1.4)
        * [leo_cache v0.6.0](https://github.com/leo-project/leo_cache/releases/tag/0.6.0)
        * [leo_commons v1.1.0](https://github.com/leo-project/leo_commons/releases/tag/1.1.0)
        * [leo_dcerl v0.2.11](https://github.com/leo-project/leo_dcerl/releases/tag/0.2.11)
        * [leo_logger v1.1.4](https://github.com/leo-project/leo_logger/releases/tag/1.1.4)
        * [leo_mcerl v0.4.1](https://github.com/leo-project/leo_mcerl/releases/tag/0.4.1)
        * [leo_mq v1.3.3](https://github.com/leo-project/leo_mq/releases/tag/1.3.3)
        * [leo_object_storage v1.2.3](https://github.com/leo-project/leo_object_storage/releases/tag/1.2.3)
        * [leo_ordning_reda v0.10.9](https://github.com/leo-project/leo_ordning_reda/releases/tag/0.10.9)
        * [leo_redundant_manager 1.9.6](https://github.com/leo-project/leo_redundant_manager/releases/tag/1.9.6)
        * [leo_rpc v0.8.10](https://github.com/leo-project/leo_rpc/releases/tag/0.8.10)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod/releases/tag/0.6.2)
        * [leo_s3_libs v1.1.5](https://github.com/leo-project/leo_s3_libs/releases/tag/1.1.5)
        * [leo_statistics v1.0.8](https://github.com/leo-project/leo_statistics/releases/tag/1.0.8)
        * [leo_watchdog v0.6.2](https://github.com/leo-project/leo_watchdog/releases/tag/0.6.2)
        * [savanna_agent v0.4.4](https://github.com/leo-project/savanna_agentreleases/tag/0.4.4)
        * [savanna_commons v0.8.6](https://github.com/leo-project/savanna_commons/releases/tag/0.8.6)
        * [erpcgen v0.2.3](https://github.com/leo-project/erpcgen/releases/tag/0.2.3)
        * [nfs_rpc_server v0.2.2](https://github.com/leo-project/nfs_rpc_server/releases/tag/0.2.2)
        * [leo_gateway v1.2.5](https://github.com/leo-project/leo_gateway/releases/tag/1.2.5)
        * [leo_manager v1.2.5](https://github.com/leo-project/leo_manager/releases/tag/1.2.5)
        * [leo_storage v1.2.5](https://github.com/leo-project/leo_storage/releases/tag/1.2.5)
    * others
        * [bitcask v1.7.1](https://github.com/leo-project/bitcask/releases/tag/1.7.1)
        * [cowboy v1.0.0](https://github.com/extend/cowboy/releases/tag/1.0.0)
        * [cowlib v1.0.0](https://github.com/extend/cowboy/releases/tag/1.0.0)
        * [elarm v0.3.0](https://github.com/leo-project/elarm/releases/tag/0.3.0)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb/releases/tag/1.4.10)
        * [folsom v0.8.1](https://github.com/boundary/folsom/releases/tag/0.8.1)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy/releases/tag/0.2.2)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4/releases/tag/0.2.2) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.2.4 (Jan 23, 2015)
====================

* Fixed Bugs
    * [#297](https://github.com/leo-project/leofs/issues/297) ``leo_object_storage`` Could NOT handle delete requests which made by the MQ mechanism at LeoFS v1.2.3

* Used libraries
    * leo project
        * [leo_backend-db v1.1.4](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.6.0](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.1.0](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.11](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.1.4](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.4.1](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.3.3](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.2.3](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.9](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager 1.9.5](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.10](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.1.5](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.8](https://github.com/leo-project/leo_statistics.git)
        * [leo_watchdog v0.6.1](https://github.com/leo-project/leo_watchdog.git)
        * [savanna_agent v0.4.4](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.8.6](https://github.com/leo-project/savanna_commons.git)
        * [erpcgen v0.2.3](https://github.com/leo-project/erpcgen.git)
        * [nfs_rpc_server v0.2.2](https://github.com/leo-project/nfs_rpc_server.git)
        * [leo_gateway v1.2.4](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.2.4](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.2.4](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.7.1](https://github.com/leo-project/bitcask.git)
        * [cowboy v1.0.0](https://github.com/extend/cowboy.git)
        * [cowlib v1.0.0](https://github.com/extend/cowboy.git)
        * [elarm v0.3.0](https://github.com/leo-project/elarm.git)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.2.3 (Jan 20, 2015)
====================

* Improvements
    * [#285](https://github.com/leo-project/leofs/issues/285) ``leo_storage`` Implemented "cluster-watchdog" in order to keep best condition of a cluster
    * [#286](https://github.com/leo-project/leofs/issues/286) ``leo_storage`` Unified name of configuration items for the mq and the compaction
* Fixed Bugs
    * [#288](https://github.com/leo-project/leofs/issues/288) ``leo_manager`` Fixed wrong mix/max values when issueing [the status &lt;storage-node&gt; command](http://leo-project.net/leofs/docs/admin_guide/admin_guide_2.html#status-command) with ``leofs-adm command``
    * [#290](https://github.com/leo-project/leofs/issues/290) [the du detail &lt;storage-node&gt; command](http://leo-project.net/leofs/docs/admin_guide/admin_guide_5.html#du-detail) with ``leofs-adm command`` had broken 1.2.2
    * [#292](https://github.com/leo-project/leofs/issues/292) ``leo_storage`` [proc_lib:start_link](http://erlang.org/doc/man/proc_lib.html#spawn_link-1) must be used instead of [erlang:spawn](http://erlang.org/doc/man/erlang.html#spawn-1)
    * [#293](https://github.com/leo-project/leofs/issues/293) Fixed that remain objects after finished data-compaction, situation of which is combination auto-compaction and deletion of a bucket
* Used libraries
    * leo project
        * [leo_backend-db v1.1.4](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.6.0](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.1.0](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.11](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.1.4](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.4.1](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.3.3](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.2.2](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.9](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager 1.9.5](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.10](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.1.5](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.8](https://github.com/leo-project/leo_statistics.git)
        * [leo_watchdog v0.6.1](https://github.com/leo-project/leo_watchdog.git)
        * [savanna_agent v0.4.4](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.8.6](https://github.com/leo-project/savanna_commons.git)
        * [erpcgen v0.2.3](https://github.com/leo-project/erpcgen.git)
        * [nfs_rpc_server v0.2.2](https://github.com/leo-project/nfs_rpc_server.git)
        * [leo_gateway v1.2.3](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.2.3](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.2.3](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.7.1](https://github.com/leo-project/bitcask.git)
        * [cowboy v1.0.0](https://github.com/extend/cowboy.git)
        * [cowlib v1.0.0](https://github.com/extend/cowboy.git)
        * [elarm v0.3.0](https://github.com/leo-project/elarm.git)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)



1.2.2 (Dec 17, 2014)
====================

* New Features
    * [#117](https://github.com/leo-project/leofs/issues/117) ``leo_storage`` Implemented the auto-compaction mechanism
      * The auto-compaction configuration file for [LeoFS Storage](https://github.com/leo-project/leo_storage/blob/develop/priv/leo_storage.conf#L139-L152), name of which is ``leo_storage.conf``
      * The auto-compaction configuration is as follows:
      ```bash
      ## [compaction] enabled compaction? - default:false
      autonomic_op.compaction.is_enabled = true

      ## [compaction] number of parallel procs - default:1
      autonomic_op.compaction.parallel_procs = 1

      ## [compaction] warning ratio of active size - default:70%
      autonomic_op.compaction.warn_active_size_ratio = 70

      ## [compaction] threshold ratio of active size - default:60%
      autonomic_op.compaction.threshold_active_size_ratio = 60
      ```
* Improvements
    * [#270](https://github.com/leo-project/leofs/issues/270) Supported leo_watchdog for FreeBSD and SmartOS
    * [#281](https://github.com/leo-project/leofs/issues/281) ``leo_gateway`` Made timeout configurable for the get and the find_by_parent_dir
    * The watchdog mechnism to production status
      * The watchdog configuration file for [LeoFS Storage](https://github.com/leo-project/leo_storage/blob/develop/priv/leo_storage.conf#L63-L136) and [LeoFS Gateway](https://github.com/leo-project/leo_gateway/blob/develop/priv/leo_gateway.conf#L161-L206), name of which are ``leo_storage.conf`` and ``leo_gateway.conf``
      * The watchdog configuration for CPU and Disk as follows:
      ```bash
      ##  Watchdog.CPU
      ##
      ## Is cpu-watchdog enabled - default:false
      watchdog.cpu.is_enabled = true

      ## cpu - raised error times
      watchdog.cpu.raised_error_times = 3

      ## cpu - watch interval - default:5sec
      watchdog.cpu.interval = 5

      ## Threshold CPU load avg for 1min/5min - default:5.0
      watchdog.cpu.threshold_cpu_load_avg = 5.0

      ## Threshold CPU load util - default:100 = "100%"
      watchdog.cpu.threshold_cpu_util = 100

      ##  Watchdog.DISK
      ##
      ## Is disk-watchdog enabled - default:false
      watchdog.disk.is_enabled = true

      ## disk - raised error times
      watchdog.disk.raised_error_times = 3

      ## disk - watch interval - default:1sec
      watchdog.disk.interval = 1

      ## Threshold disk use% - defalut:85%
      watchdog.disk.threshold_disk_use = 85

      ## Threshold disk util% - defalut:100%
      watchdog.disk.threshold_disk_util = 100

      ## Threshold disk read kb/sec - defalut:262144(KB)
      watchdog.disk.threshold_disk_rkb = 262144

      ## Threshold disk write kb/sec - defalut:262144(KB)
      watchdog.disk.threshold_disk_wkb = 262144

      ## disk target devices for checking disk utilization
      watchdog.disk.target_devices = []
      ```
      * Improved MQ's confurations for LeoFS Stroage in order to be able to control system load
      ```bash
      ## [Number of bach processes of message]
      ##
      ## Minimum number of bach processes of message
      mq.num_of_batch_process_min = 100

      ## Maxmim  number of bach processes of message
      mq.num_of_batch_process_max = 10000

      ## Maxmim  number of bach processes of message
      mq.num_of_batch_process_regular = 1000

      ## Maxmim  number of bach processes of message
      mq.num_of_batch_process_step = 250

      ## [Interval beween batch-procs]
      ##
      ## Minimum value of interval beween batch-procs(msec)
      mq.interval_between_batch_procs_min = 10

      ## Maximum value of interval between batch-procs(msec)
      mq.interval_between_batch_procs_max = 1000

      ## Regular value of interval between batch-procs(msec)
      mq.interval_between_batch_procs_regular = 300

      ## Step value of interval between batch-procs(msec)
      mq.interval_between_batch_procs_step = 100
      ```
      * Improved the ``mq-status`` command of ``leofs-adm``
      ```bash
      $ leofs-adm mq-stats storage_1@127.0.0.1
                    id                |    state    | number of msgs | batch of msgs  |    interval    |            description
      --------------------------------+-------------+----------------|----------------|----------------|-----------------------------------
      leo_delete_dir_queue            |   idling    | 0              | 1000           | 100            | delete directories
      leo_comp_meta_with_dc_queue     |   idling    | 0              | 1000           | 100            | compare metadata w/remote-node
      leo_sync_obj_with_dc_queue      |   idling    | 0              | 1000           | 100            | sync objs w/remote-node
      leo_recovery_node_queue         |   idling    | 0              | 1000           | 100            | recovery objs of node
      leo_async_deletion_queue        |   idling    | 0              | 1000           | 100            | async deletion of objs
      leo_rebalance_queue             |   running   | 2167           | 1400           | 10             | rebalance objs
      leo_sync_by_vnode_id_queue      |   idling    | 0              | 1000           | 100            | sync objs by vnode-id
      leo_per_object_queue            |   idling    | 0              | 1000           | 100            | recover inconsistent objs
       ```
* Fixed Bugs
    * [#273](https://github.com/leo-project/leofs/issues/273) ``leo_gateway`` ``NFS`` Max file size was hardcoded as 4GB
    * [#274](https://github.com/leo-project/leofs/issues/274) ``leo_manager`` ``leo_storage`` ``leo_gateway`` Crashed a manager node by snmp-related issue with Erlang-17
    * [#275](https://github.com/leo-project/leofs/issues/275) ``leo_gateawy`` An error message was output if there is no the http custom header file
    * [#277](https://github.com/leo-project/leofs/issues/277) ``leo_gateway`` In REST mode, Putting a large object failed
    * [#279](https://github.com/leo-project/leofs/issues/279) ``leo_object_storage`` Compaction status can be inconsistent when an error occured while preparing compaction
    * [#282](https://github.com/leo-project/leofs/issues/282) ``leo_gateway`` Gateway's timeout configuration has been ignored
* Used libraries
    * leo project
        * [leo_backend-db v1.1.4](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.6.0](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.1.0](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.11](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.1.4](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.4.1](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.3.0](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.2.0](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.9](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager 1.9.2](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.10](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.1.5](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.7](https://github.com/leo-project/leo_statistics.git)
        * [leo_watchdog v0.6.0](https://github.com/leo-project/leo_watchdog.git)
        * [savanna_agent v0.4.4](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.8.6](https://github.com/leo-project/savanna_commons.git)
        * [erpcgen v0.2.3](https://github.com/leo-project/erpcgen.git)
        * [nfs_rpc_server v0.2.2](https://github.com/leo-project/nfs_rpc_server.git)
        * [leo_gateway v1.2.2](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.2.2](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.2.2](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.7.1](https://github.com/leo-project/bitcask.git)
        * [cowboy v1.0.0](https://github.com/extend/cowboy.git)
        * [cowlib v1.0.0](https://github.com/extend/cowboy.git)
        * [elarm v0.3.0](https://github.com/leo-project/elarm.git)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.2.1 (Nov 11, 2014)
====================

* Improvements
    * Supported [LeoCenter](https://github.com/leo-project/leo_center) for LeoFS v1.2
* Fixed Bugs
    * Fixed system migration issue from v1.x to v1.2.0

* Used libraries
    * leo project
        * [leo_backend-db v1.1.3](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.6.0](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.1.0](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.11](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.1.3](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.4.1](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.2.0](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.1.8](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.9](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager 1.9.1](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.10](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.1.4](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.7](https://github.com/leo-project/leo_statistics.git)
        * [leo_watchdog v0.4.1](https://github.com/leo-project/leo_watchdog.git)
        * [savanna_agent v0.4.4](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.8.6](https://github.com/leo-project/savanna_commons.git)
        * [erpcgen v0.2.3](https://github.com/leo-project/erpcgen.git)
        * [nfs_rpc_server v0.2.2](https://github.com/leo-project/nfs_rpc_server.git)
        * [leo_gateway v1.2.1](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.2.1](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.2.1](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.7.0](https://github.com/basho/bitcask.git)
        * [cowboy v1.0.0](https://github.com/extend/cowboy.git)
        * [cowlib v1.0.0](https://github.com/extend/cowboy.git)
        * [elarm v0.3.0](https://github.com/leo-project/elarm.git)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.2.0 (Nov 7, 2014)
====================

* New Features
    * Watchdog mechnism has been implemented, which is called [leo_watchdog](https://github.com/leo-project/leo_watchdog)
        * Target resources: [cpu, io, disk]
        * Status: Beta
        * Requirements: CentOS-6.5 later and Ubuntu-13.10/14.04 later
        * Furure plan: Support FreeBSD and SmartOS with v1.2.1
* Improvements
    * [#121](https://github.com/leo-project/leofs/issues/121) Tool to migrate metadata dbs from bitcask to leveldb
    * [#166](https://github.com/leo-project/leofs/issues/166) ``leo_rpc`` ``leo_storage`` Multi DC replication messages could lost
    * [#202](https://github.com/leo-project/leofs/issues/202) ``leo_gateway`` Made timeout configurable
    * [#239](https://github.com/leo-project/leofs/issues/239) ``leo_gateway`` Added custom HTTP header for CDN integration
    * [#255](https://github.com/leo-project/leofs/issues/255) ``leo_gateway`` Made a PUT request in parallel when handling a large object
    * [#256](https://github.com/leo-project/leofs/issues/256) ``leo_gateway`` Upgraded [Cowboy 1.0.0](https://github.com/ninenines/cowboy)
    * [#260](https://github.com/leo-project/leofs/issues/260) ``leo_gateway`` Made a MOVE request in parallel when handling a large object
    * ``leo_storage`` ``leo_mq`` Implemented to be able to operate a mq server of a storage internal
    * ``leo_storage`` Able to recursively remove objects of under directory with S3-Clients
* Fixed Bugs
    * [#262](https://github.com/leo-project/leofs/issues/262) ``leo_gateway`` ``leo_storage`` Improved RPC in order to be able to handle huge traffic with large size objects
    * [#263](https://github.com/leo-project/leofs/issues/263) ``leo_gateway`` Wrong error code when creating a bucket that already exists
    * [#265](https://github.com/leo-project/leofs/issues/265) ``leo_object_storage`` Fixed that some succeeded updates might be ignored silently while executing compaction
    * [#268](https://github.com/leo-project/leofs/issues/265) ``leo_object_storage`` Fixed that wrong output format of data-diagnosis when including children of an large-object

* Used libraries
    * leo project
        * [leo_backend-db v1.1.3](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.6.0](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.1.0](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.11](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.1.3](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.4.1](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.2.0](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.1.8](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.9](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager 1.9.1](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.10](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.1.4](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.7](https://github.com/leo-project/leo_statistics.git)
        * [leo_watchdog v0.4.1](https://github.com/leo-project/leo_watchdog.git)
        * [savanna_agent v0.4.4](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.8.6](https://github.com/leo-project/savanna_commons.git)
        * [erpcgen v0.2.3](https://github.com/leo-project/erpcgen.git)
        * [nfs_rpc_server v0.2.2](https://github.com/leo-project/nfs_rpc_server.git)
        * [leo_gateway v1.2.0](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.2.0](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.2.0](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.7.0](https://github.com/basho/bitcask.git)
        * [cowboy v1.0.0](https://github.com/extend/cowboy.git)
        * [cowlib v1.0.0](https://github.com/extend/cowboy.git)
        * [elarm v0.3.0](https://github.com/leo-project/elarm.git)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.1.5 (Oct 15, 2014)
====================

* Improvements
    * [#253](https://github.com/leo-project/leofs/issues/253) ``leo_manager`` Inform administrators via a log if the number of replica is changed
    * ``leo_logger`` Implemented that it remove a zero-byte log when closing/rotating
* Fixed Bugs
    * [#254](https://github.com/leo-project/leofs/issues/254) ``leo_redundant_manager`` Failed creating RING on cheap VM environment
* Used libraries
    * leo project
        * [leo_backend-db v1.1.2](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.6.0](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.1.0](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.11](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.1.3](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.4.1](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.0.10](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.1.5](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.9](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager 1.9.0](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.10](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.1.3](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.7](https://github.com/leo-project/leo_statistics.git)
        * [savanna_agent v0.4.4](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.8.6](https://github.com/leo-project/savanna_commons.git)
        * [erpcgen v0.2.3](https://github.com/leo-project/erpcgen.git)
        * [nfs_rpc_server v0.2.2](https://github.com/leo-project/nfs_rpc_server.git)
        * [leo_gateway v1.1.5](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.1.5](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.1.5](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.7.0](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [cowlib v0.6.2](https://github.com/extend/cowboy.git)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.1.4 (Oct 3, 2014)
====================

* Improvements
    * Strictly checked routing-table between manager-node and other nodes
    * Implemented the data diagnosis function of a storage-node
    * [#249](https://github.com/leo-project/leofs/issues/249) ``leo_manager`` Improve whereis command
* Fixed Bugs
    * [#246](https://github.com/leo-project/leofs/issues/246) ``leo_storage`` Could not recursively creating directory
    * [#247](https://github.com/leo-project/leofs/issues/247) ``leo_storage`` Start normally even if error occur
    * [#250](https://github.com/leo-project/leofs/issues/250) ``leo_statistics`` leo_statistics_sampler can be down under very high load
* Used libraries
    * leo project
        * [leo_backend-db v1.1.2](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.6.0](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.1.0](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.11](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.1.2](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.4.1](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.0.10](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.1.5](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.9](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager 1.8.9](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.10](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.1.3](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.7](https://github.com/leo-project/leo_statistics.git)
        * [savanna_agent v0.4.4](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.8.6](https://github.com/leo-project/savanna_commons.git)
        * [erpcgen v0.2.3](https://github.com/leo-project/erpcgen.git)
        * [nfs_rpc_server v0.2.2](https://github.com/leo-project/nfs_rpc_server.git)
        * [leo_gateway v1.1.4](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.1.4](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.1.4](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.7.0](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [cowlib v0.6.2](https://github.com/extend/cowboy.git)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.1.3 (Sep 12, 2014)
====================

* Improved
    * Implement the "rollback" command, which is able to rollback state of a storage node from 'detach' to 'running'
* Fixed Bugs
    * [#236](https://github.com/leo-project/leofs/issues/236) ``leo_redundant_manager`` - storage node empty after 1.1.2 update and compaction
    * [#237](https://github.com/leo-project/leofs/issues/237) ``leo_manager`` - Cannot complete the re-balance objects and the recover-node command
    * [#238](https://github.com/leo-project/leofs/issues/238) ``leo_manager`` - Failed to migrate mnesia data when upgrading LeoFS from pre2 to 1.1.2
    * [#241](https://github.com/leo-project/leofs/issues/241) ``leo_gateway`` - Change the default ram cache capasity from 1GB to 256MB
    * [#242](https://github.com/leo-project/leofs/issues/242) ``leo_gateway`` - leo_garteway process could be down when receiving an invalid request
    * [#243](https://github.com/leo-project/leofs/issues/243) ``leo_storage`` - leo_gateway could respond 500 instead of 404
* Used libraries
    * leo project
        * [leo_backend-db v1.1.1](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.24](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.0.5](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.10](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.0.5](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.4.0](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.0.9](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.1.3](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.8](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.8.8](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.9](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.1.2](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.6](https://github.com/leo-project/leo_statistics.git)
        * [savanna_agent v0.4.3](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.8.5](https://github.com/leo-project/savanna_commons.git)
        * [erpcgen v0.2.3](https://github.com/leo-project/erpcgen.git)
        * [nfs_rpc_server v0.2.2](https://github.com/leo-project/nfs_rpc_server.git)
        * [leo_gateway v1.1.3](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.1.3](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.1.3](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.7.0](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [cowlib v0.6.2](https://github.com/extend/cowboy.git)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.1.2 (Sep 4, 2014)
===================

* Improved
    * ``leo_object_storage`` - Improved the compaction mechanism
        * It absolutely minimized time required for lock of a storage during data-compaction
* Fixed Bugs
    * [#225](https://github.com/leo-project/leofs/issues/225) ``leo_manager`` - The history command may cause VM to crash
        * We've provided the [tools/vacuum_history](https://github.com/leo-project/leofs_utils/tree/develop/tools/vacuum_history)
    * [#229](https://github.com/leo-project/leofs/issues/229) ``leo_gateway`` - Can't upload file name with space or other character got 403 forbidden
    * [#230](https://github.com/leo-project/leofs/issues/230) ``leo_gateway`` - COPY request fail when the source path include urlencoded characters
    * [#234](https://github.com/leo-project/leofs/issues/234) ``leo_gateway`` - Unexpected error may occur when responding 403/404
    * [#235](https://github.com/leo-project/leofs/issues/235) ``leo_storage`` - MDC replication could cause VM to crash (in narrow band width network - 100Mbps)
* Used libraries
    * leo project
        * [leo_backend-db v1.1.1](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.24](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.0.5](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.10](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.0.5](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.4.0](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.0.9](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.1.3](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.8](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.8.7](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.9](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.1.2](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.6](https://github.com/leo-project/leo_statistics.git)
        * [savanna_agent v0.4.3](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.8.5](https://github.com/leo-project/savanna_commons.git)
        * [erpcgen v0.2.3](https://github.com/leo-project/erpcgen.git)
        * [nfs_rpc_server v0.2.2](https://github.com/leo-project/nfs_rpc_server.git)
        * [leo_gateway v1.1.2](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.1.2](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.1.2](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.7.0](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [cowlib v0.6.2](https://github.com/extend/cowboy.git)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.1.1 (Aug 21, 2014)
=========================

* Improved
    * [leofs-adm](https://github.com/leo-project/leofs/blob/master/leofs-adm)
        * Supported FreeBSD
        * Able to set *host* and *port* of the Manager node
    * The compaction mechanism
        * Added *raw-file-path* in collapsed-object-log during executing data-compaction
* Fixed Bugs
    * [#219](https://github.com/leo-project/leofs/issues/219) ``leo_gateway`` ``leo_s3_libs`` - Access Denied error when putting a file to a bucket with the same name
    * [#222](https://github.com/leo-project/leofs/issues/222) ``leo_gateway`` - Discard unnecessary object with the compaction after failure of storing a large object
    * [#223](https://github.com/leo-project/leofs/issues/223) ``leo_object_storage`` - Not match checksum of an large-object-parent after executed the rebalance command and the recover-node command
    * ``leo_manager`` - Manager node could not modify Gateway node's ring-hash.
        * The issue appeared v1.1.0.
    * ``leo_object_storage`` - The compaction command might fail when an object container has broken objects at its head
        * It's absolutely rare case
    * ``leo_redundant_manager`` - Manager could not generate RING when taking over objects from a detach-node to a attach-node (a new node)
* Used libraries
    * leo project
        * [leo_backend-db v1.0.8](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.23](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.0.4](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.10](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.0.4](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.4.0](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.0.8](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.1.2](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.5](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.8.6](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.8](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.1.1](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.5](https://github.com/leo-project/leo_statistics.git)
        * [savanna_agent v0.4.2](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.8.4](https://github.com/leo-project/savanna_commons.git)
        * [erpcgen v0.2.3](https://github.com/leo-project/erpcgen.git)
        * [nfs_rpc_server v0.2.2](https://github.com/leo-project/nfs_rpc_server.git)
        * [leo_gateway v1.1.1](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.1.1](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.1.1](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.7.0](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [cowlib v0.6.2](https://github.com/extend/cowboy.git)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.1.0 (Aug 6, 2014)
=========================

* New Features
    * Implement [NFS Support](http://leo-project.net/leofs/docs/configuration_5.html) as one of LeoFS protocols, which is the alpha version.
        * We have checked this mechanism with *CentOS 6.5* and *Ubuntu Server 14.04 LTS* but we're goinng to investigate other OS such as *FreeBSD* and *SmartOS*.
        * **NOTE:** Changed [the configuration of the protocol](https://github.com/leo-project/leo_gateway/blob/develop/priv/leo_gateway.conf#L46) from ``http.handler`` to ``protocol``
    * The  [leofs-adm](https://github.com/leo-project/leofs/blob/master/leofs-adm) script
        * This command makes administrative operations of LeoFS very easy.
* Improved
    * Refactored all libraries and applications using *dialyzer*
* Fixed Bugs
    * [#142](https://github.com/leo-project/leofs/issues/142) ``leo_manager`` - Unknown Behavior - Could not retrieve RING
    * [#193](https://github.com/leo-project/leofs/issues/193) ``leo_gateway`` - PUT with REPLACE could leave a source file
    * [#199](https://github.com/leo-project/leofs/issues/199) ``leo_storage`` - An object in a sub directory (2 layer and over) could not be removed with DragonDisk
    * [#207](https://github.com/leo-project/leofs/issues/207) ``leo_object_storage`` - Compaction may fail when an AVS is corrupted
    * [#208](https://github.com/leo-project/leofs/issues/208) ``leo_object_storage`` - Compaction may leave stale objects which size are larger than the chunk size
    * ``leo-storage`` Multi data center replication may fail without notifying errors under a narrow bandwidth and very high-load.

* Used libraries
    * leo project
        * [leo_backend-db v1.0.8](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.23](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.0.4](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.10](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.0.4](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.4.0](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.0.8](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.1.0](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.5](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.8.4](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.8](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.6.2](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.1.0](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.4](https://github.com/leo-project/leo_statistics.git)
        * [savanna_agent v0.4.2](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.8.4](https://github.com/leo-project/savanna_commons.git)
        * [erpcgen v0.2.2](https://github.com/leo-project/erpcgen.git)
        * [nfs_rpc_server v0.2.1](https://github.com/leo-project/nfs_rpc_server.git)
        * [leo_gateway v1.1.0](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.1.0](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.1.0](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.7.0](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [cowlib v0.6.2](https://github.com/extend/cowboy.git)
        * [eleveldb v1.4.10](https://github.com/basho/eleveldb.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.2.2](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.0.2 (May 9, 2014)
=========================

* Fixed Bugs
    * [#189](https://github.com/leo-project/leofs/issues/189) ``leo_object_storage`` - Actual disk usage is different from the manager-console.
    * [#188](https://github.com/leo-project/leofs/issues/188) ``leo_object_storage`` - When existing large objects in a leo_storage, data loss of which happend with the compaction command.
* Used libraries
    * leo project
        * [leo_backend-db v1.0.3](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.20](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.0.1](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.7](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.0.2](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.9](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.0.3](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.0.4](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.3](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.8.1](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.3](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.6.0](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.0.1](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.x](https://github.com/leo-project/leo_statistics.git)
        * [savanna_agent v0.2.2](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.6.3](https://github.com/leo-project/savanna_commons.git)
        * [leo_gateway v1.0.2](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.0.2](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.0.2](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.7](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [eleveldb v1.4.7](https://github.com/basho/eleveldb.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.0.1 (May 8, 2014)
=========================

* Improved
    * [#183](https://github.com/leo-project/leofs/issues/183) ``leo_storage`` - Replication messages could be sent between storage nodes more than necessary
    * [#176](https://github.com/leo-project/leofs/issues/176) ``leo_center``  - Supported LeoFS v1.0
    * [#167](https://github.com/leo-project/leofs/issues/167) ``leo_storage`` - Automatically synchronization of objects between a local cluster and another remote cluster could fail
    * [#165](https://github.com/leo-project/leofs/issues/165) ``leo_manager`` - Could not modify ``cluster_id``, ``dc_id`` after leo_manger started
    * [#140](https://github.com/leo-project/leofs/issues/140) ``leo_gateway`` - Supported for ``s3gof3r`` as S3-Client
* Fixed Bugs
    * Corrected termination of applications
    * [#187](https://github.com/leo-project/leofs/issues/187) ``leo_storage`` - Could not work the ``rebalance`` and ``recover`` command
    * [#186](https://github.com/leo-project/leofs/issues/186) ``leo_storage`` - Could not correctly finish the ``compaction`` command when exists large-objects
    * [#185](https://github.com/leo-project/leofs/issues/185) ``leo_manager`` - Failed to execute the ``delete-endpoint`` command
    * [#184](https://github.com/leo-project/leofs/issues/183) ``leo_manager`` - Failed to execute the ``update-acl`` command
    * [#182](https://github.com/leo-project/leofs/issues/182) ``leo_manager`` - When status of a storage is ``restarted``, issuing compaction could cause data loss
    * [#173](https://github.com/leo-project/leofs/issues/173) ``leo_manager`` - Could not migrate data from leofs-1.0.0-pre3 ro leofs-1.0.0
    * [#171](https://github.com/leo-project/leofs/issues/171) ``leo_gateway`` - Head-method with PHP client could not work.
    * [#160](https://github.com/leo-project/leofs/issues/160) ``leo_manager`` - Failed to upgrade from v0.14.6 to v1.0.0
    * [#153](https://github.com/leo-project/leofs/issues/153) ``leo_gateway`` - When using s3cmd, GET operation for larger than 5MB object gives error at leo_gateway
* Used libraries
    * leo project
        * [leo_backend-db v1.0.3](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.20](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.0.1](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.7](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.0.2](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.9](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.0.3](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.0.3](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.3](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.8.1](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.3](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.6.0](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.0.1](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.x](https://github.com/leo-project/leo_statistics.git)
        * [savanna_agent v0.2.2](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.6.3](https://github.com/leo-project/savanna_commons.git)
        * [leo_gateway v1.0.1](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.0.1](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.0.1](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.7](https://github.com/basho/bitcask.git)
        * [eleveldb v1.4.7](https://github.com/basho/eleveldb.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.0.0 (Apr 2, 2014)
=========================

* New features
    * Multi datacenter replication (1st phase)
        * Realized async-replication between clusters
            * After sent stacked objects to a remote-cluster, receive the list of metadatas from a remote-cluster, then compare them with local-cluster. Eventually, an inconsistent object is recovered.
            * Provided easy operation of multi-datacenter replication with leo-manager's console
            * After joined a new cluster, automatically synchronize objects between local-cluster and a remote-cluster
        * Provided ``recover cluster`` which is able to fix inconsistency objects with remote-cluster
    * [#139](https://github.com/leo-project/leofs/issues/139) Implemented the Bucket ACL
* Improved
    * ``leo_backend_db`` Bump bitcask to v1.6.7
    * ``leo_object_storage`` Updated compaction, handling an object for the multi-dc replication
    * ``leo_ordning_reda`` Updated handle-send interface for the multi-dc replication
    * ``leo_rpc`` Improved to check-in pools into leo_pod
* Fixed Bugs
    * [#144](https://github.com/leo-project/leofs/issues/143) - Failure occurred when running snmpwalk
    * [#146](https://github.com/leo-project/leofs/issues/146) - No retry when receiving a head request
    * [#148](https://github.com/leo-project/leofs/issues/148) - AWS-clients of PHP and Node.js could not copy object properly copied file became 0byte
    * [#151](https://github.com/leo-project/leofs/issues/151) - ``whereis-command`` had not been recorded on history table
    * [#162](https://github.com/leo-project/leofs/issues/162) - Able to get removed user on the manager-console
    * [#163](https://github.com/leo-project/leofs/issues/163) - ``update-acl`` and ``get-acl`` methods unexpected to display the permission messages
* Used libraries
    * leo project
        * [leo_backend-db v1.0.2](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.20](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.0.1](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.7](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.0.1](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.9](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.0.2](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.0.1](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.2](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.8.0](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.2](https://github.com/leo-project/leo_rpc.git)
        * [leo_pod v0.4.8](https://github.com/leo-project/leo_pod.git)
        * [leo_s3_libs v1.0.1](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.1](https://github.com/leo-project/leo_statistics.git)
        * [savanna_agent v0.2.1](https://github.com/leo-project/savanna_agent.git)
        * [savanna_commons v0.6.2](https://github.com/leo-project/savanna_commons.git)
        * [APPLICATION]
        * [leo_gateway v1.0.0](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.0.0](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.0.0](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.7](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.0.0-pre3 (Feb 20, 2014)
=========================

* Improved
    * `leo_manager` Able to plug functions in order to realize to build another manager
    * `leo_redundant_manager` Improved the performance of the membership and the rebalance
    * `leo_redundant_manager` Modified that restrict membership of a node, the state of which is not running
    * `leo_statistics` Switch the function of statistics to [savanna_commons](https://github.com/leo-project/savanna_commons), which isan Erlang based metrics server.
    * `leo_ordning_reda` Improved the function of object stacking
    * `leo_ordning_reda` Improved efficiency of termination of a process
* Fixed Bugs
    * `leo_gateway` Fixed to escape xml elements correctly with xmerl_lib:export_text
    * `leo_gateway` Modified the http response body format when responding a http error status according to the S3 spec(http://docs.aws.amazon.com/AmazonS3/latest/API/ErrorResponses.html#RESTErrorResponses)
    * `leo_manager` [#116](https://github.com/leo-project/leofs/issues/116) Implement new sync mechanism in Manager, which is able to maintain hard consistency of the rings
    * `libcutil (cache-lib)` [#123](https://github.com/leo-project/leofs/issues/123) Add `-fPIC` to CFLAGS
    * `leo_backend_db` [#129](https://github.com/leo-project/leofs/issues/129) Fixed to remove all files in a bucket when deleting it(only occured in case using leveldb as metadata storage)
    * `leo_gateway` [#130](https://github.com/leo-project/leofs/issues/130) Fixed wrong access log formats when operationg a large-object
    * `leo_manager`,`leo_storage`,`leo_gateway` [#131](https://github.com/leo-project/leofs/issues/131) Wrote the version number in the source of configurations
    * `leo_gateway` [#136](https://github.com/leo-project/leofs/issues/136) Support that move and copy a large object with S3-Client(s)
    * `leo_object_storage` Fixed to handle invalid data blocks while doing compaction
    * `leo_rpc` Fixed to close a tcp socket properly in any cases
    * `leo_gateway` [#140](https://github.com/leo-project/leofs/issues/140) Fixed to return 206 status when responding a partial body
* Used libraries
    * leo project
        * [leo_backend-db v1.0.0](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.19](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v1.0.0](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.7](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v1.0.0](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.9](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v1.0.0](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v1.0.0](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.10.0](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_pod v0.4.7](https://github.com/leo-project/leo_pod.git)
        * [leo_redundant_manager v1.4.1](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.8.0](https://github.com/leo-project/leo_rpc.git)
        * [leo_s3_libs v0.12.28](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v1.0.0](https://github.com/leo-project/leo_statistics.git)
        * [savanna_commons v0.4.3](https://github.com/leo-project/savanna_commons.git)
        * [leo_gateway v1.0.0-pre3](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.0.0-pre3](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.0.0-pre3](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.7](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [eleveldb v1.4.7](https://github.com/basho/eleveldb)
        * [folsom v0.8.1](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.0.0-pre2 (Jan 22, 2014)
=========================

* New Features
     * Implemented for Multi DC Replication
         * Synchronize configuration and staus of remote cluster(s) after joined each other
         * Regularly check status of remote cluster(s)
         * Add the commands of Multi DC Replication in Manager
              * 'join-cluster' and 'remove-cluster'
* Improved
     * The performance of the prefix search, which like a "ls"
     * Changed format of the metadata because of improvement of the prefix search
     * Removed Elasticsearch integration in the logger
* Fixed Bugs
     * Unexpected response from leo_storage to leo_gateway when an object wan not found
     * Respond an error with deletion of an object when it was not found
* Used libraries
    * leo project
        * [leo_backend-db v0.14.5](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.17](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.14.10](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.7](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v0.12.8](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.9](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v0.12.25](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v0.14.11](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.8.19](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_pod v0.4.7](https://github.com/leo-project/leo_pod.git)
        * [leo_redundant_manager v1.4.0](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_rpc v0.6.2](https://github.com/leo-project/leo_rpc.git)
        * [leo_s3_libs v0.12.27](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.14.9](https://github.com/leo-project/leo_statistics.git)
        * [leo_gateway v1.0.0-pre2](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.0.0-pre2](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.0.0-pre2](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.4](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom v0.8.0](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


1.0.0-pre1 (Dec 27, 2013)
=========================

* Improved
   * Revised the replicator and the read-repairer for the multi data center replicaion
   * [#113](https://github.com/leo-project/leofs/issues/113) Modified the configuration of limit of large-object length
      * "limit length" = ${large_object.chunked_obj_len} * ${large_object.max_chunked_objs}
   * Improve the function of "rebalance-command"
   * Improve the function of "start-command"
   * Added "dump-ring" on the manager console
* Fixed Bugs
   * Fixed that a rebalance msg can be lost during rebalance with a 0.02% possibility
   * Fixed that not retrieved a bucket-info when stopping all managers
* Used libraries
    * leo project
        * [leo_backend-db v0.14.2](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.16](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.14.9](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.7](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v0.12.6](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.9](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v0.12.23](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v0.14.8](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.8.18](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.2.6](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.25](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.14.8](https://github.com/leo-project/leo_statistics.git)
        * [leo_gateway v1.0.0-pre1](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v1.0.0-pre1](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v1.0.0-pre1](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.4](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom v0.8.0](https://github.com/boundary/folsom.git)
        * [jiffy v0.8.5](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.16.8 (Dec 12, 2013)
=====================

* Improved
  * [#109](https://github.com/leo-project/leofs/issues/109) Moved to "ini-file" configuration, which no longer use Erlang-specific syntax. Using [cuttlefish](https://github.com/basho/cuttlefish) to realize this function.
  * [#110](https://github.com/leo-project/leofs/issues/110) Supported [erlcloud](https://github.com/gleber/erlcloud) for Erlang users
  * [Supported Mac OS X](https://github.com/leo-project/libcutil/pull/2) which was contributed from Jeff Li
* Fixed Bugs
  * [#102](https://github.com/leo-project/leofs/issues/102) Happened timeout when uploading a large object
  * [#108](https://github.com/leo-project/leofs/issues/108) Happened not relocation of object(s) when removing a node and executing rebalance then add same node
  * [#111](https://github.com/leo-project/leofs/issues/111) Could not upload large size file
  * Fixed that not migrated "Bucket Table"
  * Fixed that an exception of compaction happened rarely
* Used libraries
    * leo project
        * [leo_backend-db v0.14.2](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.16](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.14.9](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.7](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v0.12.6](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.9](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v0.12.22](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v0.14.8](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.8.18](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.2.5](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.24](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.14.7](https://github.com/leo-project/leo_statistics.git)
        * [leo_gateway v0.16.8](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.16.8](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.16.8](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.4](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.16.5 (Nov 26, 2013)
=====================

* Improved
   * S3-API related
      * [#103] (https://github.com/leo-project/leofs/issues/103) Able to change password on Manager console
      * [#105] (https://github.com/leo-project/leofs/issues/105) Able to change an owner of a bucket
      * [#106] (https://github.com/leo-project/leofs/issues/106) Rename *set-endpoint* to *add-endpoint* in order to unify it and other commands
      * Multicast *update-acl* to Gateway's node(s)
      * Multicast *delete-bucket* to Gateway's node(s)
   * Other
      * Revised that manage redundant nodes toward the multi data center replication
        * Supported that manage previous and current members in a cluster in order not to happen lost data during the period of relocation of data
        * Able to recover that Manager failed to send massage of relocation from Manager to Storage(s)
        * Reduced costs of relocation of data than previous version
      * [#98] (https://github.com/leo-project/leofs/issues/98) Made a bucket name compatible with the AWS-S3 naming rule of US-region
      * [#99] (https://github.com/leo-project/leofs/issues/99) Able to set log-directory of *leo-redundant-manager*
      * Supported Ubuntu-13.10 (include Ubuntu Server 13.10)
* Fixed Bugs
  * [#94] (https://github.com/leo-project/leofs/issues/94) Happened an error when parsing XML document with S3's Java-Client
  * [#95] (https://github.com/leo-project/leofs/issues/95) Could not resume storage node
  * [#96] (https://github.com/leo-project/leofs/issues/96) Happened an error when Gateway is requested from *boto*
  * [#97] (https://github.com/leo-project/leofs/issues/97) Could not upload an object when including a bucket name in a path
  * [#100] (https://github.com/leo-project/leofs/issues/100) Broken records after update from 0.14.9 to 0.16.0
* Used libraries
    * leo project
        * [leo_backend-db v0.14.1](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.14](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.14.8](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.5](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v0.12.5](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.7](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v0.12.21](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v0.14.7](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.8.17](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.2.3](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.21](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.14.6](https://github.com/leo-project/leo_statistics.git)
        * [leo_gateway v0.16.5](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.16.5](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.16.5](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.2](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.16.0 (Oct 25, 2013)
=====================

* New Features
    * Gateway
        * Supported GET/PUT ACL a Bucket [S3-API]
        * (Beta) Able to output access-logs to Elasticsearch in order to realize to access-log analysis with Kibana
    * Other
        * Implemented SmartOS packager (Contributed by Heinz N. Gies - [Project FiFo](http://project-fifo.net/))
* Improved
    * Manager
        * Supported single 'Manager'
        * Supported to check # of detached node before executing detach-command
* Used libraries
    * leo project
        * [leo_backend-db v0.14.1](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.13](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.14.8](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.4](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v0.12.5](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.6](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v0.12.20](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v0.14.7](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.8.17](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.0.4](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.17](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.14.6](https://github.com/leo-project/leo_statistics.git)
        * [leo_gateway v0.16.0](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.16.0](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.16.0](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.2](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.14.9 (Sep 27, 2013)
=====================

* Improved
    * Supported Erlang/OTP R16B02
    * Increased performance of leo_redundant_manager

* Used libraries
    * leo project
        * [leo_backend-db v0.14.0](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.12](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.14.6](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.4](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v0.12.3](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.6](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v0.12.19](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v0.14.6](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.8.16](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.0.3](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.15](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.14.5](https://github.com/leo-project/leo_statistics.git)
        * [leo_gateway v0.14.14](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.14.9](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.14.7](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.2](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)



0.14.8 (Sep 12, 2013)
=====================

* Bugs Fixed
    * Gateway
        * Deletion failed with s3cmd in the case of not existed a targate file
        * OOM with access-log output
    * Manager
        * Start failed in the case of not reached the message from the Manager to storage-node(s)
        * Not removed a member(storage-node) when its status was 'attached'

* Used libraries
    * leo project
        * [leo_backend-db v0.12.17](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.11](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.14.4](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.3](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v0.12.2](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.5](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v0.12.18](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v0.14.5](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.8.15](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.0.2](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.14](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.14.4](https://github.com/leo-project/leo_statistics.git)
        * [leo_gateway v0.14.13](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.14.8](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.14.6](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.2](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.14.7 (Aug 23, 2013)
=====================

* Improved
    * Gateway
        * Able to output access-log

* Used libraries
    * leo project
        * [leo_backend-db v0.12.17](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.10](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.14.4](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.3](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v0.12.1](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.4](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v0.12.18](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v0.14.5](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.8.15](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.0.2](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.14](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.14.4](https://github.com/leo-project/leo_statistics.git)
        * [leo_gateway v0.14.12](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.14.7](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.14.5](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.2](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.14.6 (July 11, 2013)
======================

* Improved
    * Able to set the max number of requests allowed in a single keep-alive session

* Bugs Fixed
    * Gateway
        * Fixed to respond HTTP-headers properly when using *disk-cache*
    * Manager
        * Fixed changed status from *running* to *restarted* when restarted leo-manager

* Used libraries
    * leo project
        * [leo_backend-db v0.12.17](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.10](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.14.4](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.3](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v0.10.12](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.4](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v0.12.18](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v0.14.5](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.8.15](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.0.2](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.14](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.14.4](https://github.com/leo-project/leo_statistics.git)
        * [leo_gateway v0.14.11](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.14.6](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.14.4](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.2](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.14.5 (July 8, 2013)
=====================

* Bugs Fixed
    * Gateway
        * Gateways may respond an HTTP response with a wrong MIME type as "plain/text" when requested an uppercase filename extension such as "*.JPG" and "*.PNG" from clients
        * Fixed an error handlings properly when processing a large file with disk cache

* Used libraries
    * leo project
        * [leo_backend-db v0.12.17](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.10](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.14.4](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.3](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v0.10.12](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.4](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v0.12.18](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v0.14.5](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.8.15](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.0.2](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.14](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.14.4](https://github.com/leo-project/leo_statistics.git)
        * [leo_gateway v0.14.10](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.14.5](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.14.4](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.2](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.14.4 (June 28, 2013)
=======================

* Improved
    * Supported [Erlang/OTP R16B01](http://www.erlang.org/news/54)
    * Gateway
        * Optimize the slab size for normal use cases

* Used libraries
    * leo project
        * [leo_backend-db v0.12.16](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.9](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.14.3](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.3](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v0.10.11](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.4](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v0.12.17](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v0.14.4](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.8.14](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.0.1](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.13](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.14.3](https://github.com/leo-project/leo_statistics.git)
        * [leo_gateway v0.14.7](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.14.3](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.14.3](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.2](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.14.3 (June 21, 2013)
=======================

* Improved
    * Improved redundant-manager's performance when retrieving redundancies by up to 20%
        * Changed method of retrieving redundancies from *ets* to worker-processes
    * Make a parameter of consumption of queue's message interval into the application config
    * Replace obsolete functions *crypto:sha|md5* with *crypto:hash*

* Fixed Bugs
    * Manager
        * Some problem with bucket names format
    * Storage
        * The number of queue messages can be wrong value
            * Needed to call *bitcask:merge/1* after relaunch the storage process
        * Compaction-function can fail - "did not match data" when a target file is corrupted

* Used libraries
    * leo project
        * [leo_backend-db v0.12.16](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.8](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.14.3](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.3](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v0.10.11](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.3](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v0.12.17](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v0.14.4](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.8.14](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v1.0.1](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.13](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.14.3](https://github.com/leo-project/leo_statistics.git)
        * [leo_gateway v0.14.5](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.14.3](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.14.3](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.2](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.6](https://github.com/extend/cowboy.git)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.14.2 (June 7, 2013)
=======================

* New Features
    * Supported rack-awareness replica placement

* Improved
    * Gateway
        * Improved cache-libs, which are mem-cache and disc-cache.
            * Refactoring codes - Getting rid of duplicate codes to "libcutil"
            * Using file:sendfile/2 when retrieving an object from disk cache(dcerl)
        * Improve S3-API's compatibility
            * Supported "Range request API" for a large object
            * Supported retrieving object-list
        * Upgrade Cowboy to v0.8.5
    * Storage
        * Improved data-compaction
            * Performance tuning
            * Avoid polluting OS page caches during compaction
        * Modified the launch process
            * Able to retry connection with manager(s)
    * Manager
        * Supported to Able to remove gateway-node from manager's console when the state of specified node is ‘stop’
        * Supported system-data backup/restore (mnesia)
        * Supported taking over manager(s) for affected hardware failure
        * Supported taking over storage-node when having attach/detach nodes in operation
            * Able to take over from detach-node's files to attach-node

* Fixed Bugs
    * Gateway
        * Reply empty response unintentionally when using some s3-clients

* Used libraries
    * leo project
        * [leo_backend-db v0.12.14](https://github.com/leo-project/leo_backend_db.git)
        * [leo_cache v0.4.7](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.14.1](https://github.com/leo-project/leo_commons.git)
        * [leo_dcerl v0.2.2](https://github.com/leo-project/leo_dcerl.git)
        * [leo_logger v0.10.10](https://github.com/leo-project/leo_logger.git)
        * [leo_mcerl v0.2.2](https://github.com/leo-project/leo_mcerl.git)
        * [leo_mq v0.12.15](https://github.com/leo-project/leo_mq.git)
        * [leo_object_storage v0.14.3](https://github.com/leo-project/leo_object_storage.git)
        * [leo_ordning_reda v0.8.13](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v0.14.2](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.10](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.14.2](https://github.com/leo-project/leo_statistics.git)
        * [leo_gateway v0.14.4](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.14.2](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.14.2](https://github.com/leo-project/leo_storage.git)
    * others
        * [bitcask v1.6.2](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.5](https://github.com/extend/cowboy.git)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.14.1-1 (May 8, 2013)
=======================

* Improved
    * Gateway
        * Upgrade Ranch and Cowboy to latest version
* Fix Bugs
    * Gateway
        * Reply empty response unintentionally when using some s3 clients
            * "leo_gateway" stored a "0-byte length object" into the cache when put an large-object(over 5MB) from clients. So We supported to remove a registered object from the cache.


0.14.1 (Apr 15, 2013)
=====================

* Improved
    * Gateway
        * Commonize request-handler for easily creating APIs
        * Improve cache-controller which was replaced from ecache to leo_cache
        * Improve performance
            * Upgrade Ranch and Cowboy to latest version
    * Storage
        * Improved phased data-compaction
            * To realize non-blocking data-compaction
                * before: Making compaction per an "object-storage-file"
                * after: Making compaction per an object
    * Manager/Storage
        * Implement judgment of precondition in rebalance-comamnd
        * Implemented ``recover-command`` in Manager
            * To realize:
                * synchronize a file: ``recover file ${file-path}``
                * recover a target-node files: ``recover node ${storage-node}``
                * recover target-node RING: ``recover ring ${storage-node}``
* Fix Bugs
    * NOT worked ``s3cmd`` by degraded
    * Stored wrong file-path with REST-API by degraded

* Used libraries
    * leo project
        * [leo_cache v0.4.4](https://github.com/leo-project/leo_cache.git)
        * [leo_commons v0.12.12](https://github.com/leo-project/leo_commons.git)
        * [leo_backend-db v0.12.11](https://github.com/leo-project/leo_backend_db.git)
        * [leo_object_storage v0.14.1](https://github.com/leo-project/leo_object_storage.git)
        * [leo_mq v0.12.12](https://github.com/leo-project/leo_mq.git)
        * [leo_ordning_reda v0.8.11](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v0.12.19](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.8](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.10.11](https://github.com/leo-project/leo_statistics.git)
        * [leo_logger v0.10.8](https://github.com/leo-project/leo_logger.git)
        * [leo_gateway v0.14.1](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.14.1](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.14.1](https://github.com/leo-project/leo_storage.git)
        * [cherly v0.12.5](https://github.com/leo-project/cherly.git)
        * [dcerl v0.4.1](https://github.com/leo-project/dcerl.git)
    * others
        * [bitcask](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.3](https://github.com/extend/cowboy.git)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.14.0 (Mar 20, 2013)
=====================

* Improved
    * Upgrade Cowboy from 0.6.2(foked/add patches) to 0.8.2(original)
        * Improved put/get large-object performance
    * Support recovery of manager-status-monitor after network partition occured

* Fix bugs
    * Recovery objects (Storage)
        * Ignore ``detach-status`` from replication-message
    * Not handle ``compaction-start command`` invalid argument on Manager-console

* Used libraries
    * leo project
        * [leo_commons v0.12.11](https://github.com/leo-project/leo_commons.git)
        * [leo_backend-db v0.12.10](https://github.com/leo-project/leo_backend_db.git)
        * [leo_object_storage v0.12.29](https://github.com/leo-project/leo_object_storage.git)
        * [leo_mq v0.12.11](https://github.com/leo-project/leo_mq.git)
        * [leo_ordning_reda v0.8.10](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v0.12.18](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.7](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.10.10](https://github.com/leo-project/leo_statistics.git)
        * [leo_logger v0.10.7](https://github.com/leo-project/leo_logger.git)
        * [leo_gateway v0.14.0](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.14.0](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.14.0](https://github.com/leo-project/leo_storage.git)
        * [ecache v0.10.15](https://github.com/leo-project/ecache.git)
        * [cherly v0.12.4](https://github.com/leo-project/cherly.git)
    * others
        * [bitcask](https://github.com/basho/bitcask.git)
        * [cowboy v0.8.2](https://github.com/extend/cowboy.git)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.14.0-RC2 (Mar 14, 2013)
========================

* Improved
    * Improved cache-mechanism (Gateway)
        * Support Layered Cache, First cache-layer is RAM and Secondary cache-layer is SSD (or HDD)
        * This version realized that cache-destination is decided by object-size
             * Need to set [gateway's configuration](http://www.leofs.org/docs/install.html#leofs-gateway)

* Fix bugs
    * Incorrect judgement of active storage-node
        * Possibility of including node(s) of ``attached (status)``

* Used libraries
    * leo project
        * [leo_commons v0.12.11](https://github.com/leo-project/leo_commons.git)
        * [leo_backend-db v0.12.10](https://github.com/leo-project/leo_backend_db.git)
        * [leo_object_storage v0.12.29](https://github.com/leo-project/leo_object_storage.git)
        * [leo_mq v0.12.11](https://github.com/leo-project/leo_mq.git)
        * [leo_ordning_reda v0.8.10](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v0.12.17](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.7](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.10.10](https://github.com/leo-project/leo_statistics.git)
        * [leo_logger v0.10.7](https://github.com/leo-project/leo_logger.git)
        * [leo_gateway v0.14.0-RC2](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.14.0-RC2](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.14.0-RC2](https://github.com/leo-project/leo_storage.git)
        * [ecache v0.10.14](https://github.com/leo-project/ecache.git)
        * [cherly v0.12.4](https://github.com/leo-project/cherly.git)
    * others
        * [bitcask](https://github.com/basho/bitcask.git)
        * [cowboy v0.6.2](https://github.com/leo-project/cowboy.git) - forked from [extend/cowboy](https://github.com/extend/cowboy)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)

0.14.0-RC1 (Mar 5, 2013)
========================

* Improved
    * Improved cache-mechanism (Gateway)
        * According to improving efficiency of object-cache-pool, LeoFS-Gateway was able to store an object up to 8MB into the RAM
    * Improved data-compaction related processes (Storage, Manager)
        * Realized compact a part of data-storage, which called "phased data-compaction"
        * Realized ``suspend`` and ``resume`` data-compaction, also able to comfirm status of processes
    * Supported recovery from temporally network unlink #1 (Storage, Manager)
        * Automatically recovered target-node(s), which status transition from ``stop`` to ``running``

* Fix bugs
    * Cannot consume queueing-message(s) when storage cluster has a detached node
        * Resolved that messages of a detached node ignored

* Used libraries
    * leo project
        * [leo_commons v0.12.10](https://github.com/leo-project/leo_commons.git)
        * [leo_backend-db v0.12.9](https://github.com/leo-project/leo_backend_db.git)
        * [leo_object_storage v0.12.28](https://github.com/leo-project/leo_object_storage.git)
        * [leo_mq v0.12.9](https://github.com/leo-project/leo_mq.git)
        * [leo_ordning_reda v0.8.9](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v0.12.15](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.6](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.10.9](https://github.com/leo-project/leo_statistics.git)
        * [leo_logger v0.10.6](https://github.com/leo-project/leo_logger.git)
        * [leo_gateway v0.14.0-RC1](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.14.0-RC1](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.14.0-RC1](https://github.com/leo-project/leo_storage.git)
        * [ecache v0.10.8](https://github.com/leo-project/ecache.git)
        * [cherly v0.12.4](https://github.com/leo-project/cherly.git)
    * others
        * [bitcask](https://github.com/basho/bitcask.git)
        * [cowboy v0.6.2](https://github.com/leo-project/cowboy.git) - forked from [extend/cowboy](https://github.com/extend/cowboy)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlng-lz4)


0.12.7 (Dec 26, 2012)
---------------------

* Improve performances
    * Storage Performance Tuning#6
        * Related libs: [leo_storage, leo_object_storage]
        * Reduced compaction-cost
             * Able to execution of parallel comaction
                 * Get maximum performance by setting a appropriate number corresponding with number of cores.
* Improve
    * Gateway:
        * The optimal timeout according to file size set up.
        * Modified default cache mode from 'http' to 'inner'
    * Storage:
        * Modified completion of storage for restriction of file destruction
            * When shutting down storage, in charge of storage-process close files
        * Refactor message-queue functions
            * Unified read-failure's queue and write-failure's queue
* Fix bugs
    * Storage:
        * Overwrite an object during rebalance
            * Always check the version(clock) of object
        * Fix haystacks reopen correctly when failing compaction
    * Manager-Console
        * Crush get-endpoints when no-records
        * Crush get-users when no-records

* Used libraries
    * leo project
        * [leo_commons v0.12.6](https://github.com/leo-project/leo_commons.git)
        * [leo_backend-db v0.12.2](https://github.com/leo-project/leo_backend_db.git)
        * [leo_object_storage v0.12.16](https://github.com/leo-project/leo_object_storage.git)
        * [leo_mq v0.12.2](https://github.com/leo-project/leo_mq.git)
        * [leo_ordning_reda v0.8.5](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v0.12.4](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.2](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.10.6](https://github.com/leo-project/leo_statistics.git)
        * [leo_logger v0.10.3](https://github.com/leo-project/leo_logger.git)
        * [leo_gateway v0.12.9](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.12.9](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.12.9](https://github.com/leo-project/leo_storage.git)
        * [ecache v0.10.5](https://github.com/leo-project/ecache.git)
        * [cherly v0.12.0](https://github.com/leo-project/cherly.git)
    * others
        * [bitcask](https://github.com/basho/bitcask.git)
        * [cowboy v0.6.2](https://github.com/leo-project/cowboy.git) - forked from [extend/cowboy](https://github.com/extend/cowboy)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlang-lz4)


0.12.5 (Dec 7, 2012)
---------------------

* Improve performances
    * Storage Performance Tuning#5
        * Related libs: [leo_storage, leo_object_storage]
        * Reduced using spawn/1 in replicator #2
* Improve
    * Able to monitor VM-values on Leo Manager's console
    * Deprecate parameterized module in leo_object_storage
        * Reference: http://www.erlang.org/news/35
    * Modified re-launch storage process
        * When regularly stop the storage-process, It writes current status in a file. Then it restarts the storage-process when reading the file.
    * Able to post a large part of an object to LeoFS with multipart-upload API.
* Fix bugs
    * Respond invalid "Etag" from the gateway when using multipart-upload API.
    * Possibility of file-destruction
        * Termination of storages for the restriction of file-destruction
            * Related libs: [leo_storage, leo_object_storage]

* Used libraries
    * leo project
        * [leo_commons v0.12.6](https://github.com/leo-project/leo_commons.git)
        * [leo_backend-db v0.12.0](https://github.com/leo-project/leo_backend_db.git)
        * [leo_object_storage v0.12.12](https://github.com/leo-project/leo_object_storage.git)
        * [leo_mq v0.12.0](https://github.com/leo-project/leo_mq.git)
        * [leo_ordning_reda v0.8.4](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v0.12.1](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.12.0](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.10.6](https://github.com/leo-project/leo_statistics.git)
        * [leo_logger v0.10.2](https://github.com/leo-project/leo_logger.git)
        * [leo_gateway v0.12.6](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.12.6](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.12.6](https://github.com/leo-project/leo_storage.git)
        * [ecache v0.10.3](https://github.com/leo-project/ecache.git)
        * [cherly v0.10.2](https://github.com/leo-project/cherly.git)
    * others
        * [bitcask](https://github.com/basho/bitcask.git)
        * [cowboy v0.6.2](https://github.com/leo-project/cowboy.git) - forked from [extend/cowboy](https://github.com/extend/cowboy)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlang-lz4)


0.12.4 (Nov 21, 2012)
---------------------

* Improve performances
    * Storage Performance Tuning#4
        * Target libs: [leo_storage, leo_object_storage]
        * Reduced using spawn/1 in replicator #1
        * Used rpc:cast/4 for async-replication
* Improve
    * Able to retrieve leofs-uesrs from manager-console
    * NOT allow duplication registration of a user-account into the s3-credential
* Fix bugs
    * Fail rebalance and compaction when exists chunked objects in the storage
    * Manager-console crashed when inputed invalid parameter(s)

* Used libraries
    * leo project
        * [leo_commons v0.12.5](https://github.com/leo-project/leo_commons.git)
        * [leo_backend-db v0.10.8](https://github.com/leo-project/leo_backend_db.git)
        * [leo_object_storage v0.12.11](https://github.com/leo-project/leo_object_storage.git)
        * [leo_mq v0.10.5](https://github.com/leo-project/leo_mq.git)
        * [leo_ordning_reda v0.8.3](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v0.12.0](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.10.7](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.10.5](https://github.com/leo-project/leo_statistics.git)
        * [leo_logger v0.10.1](https://github.com/leo-project/leo_logger.git)
        * [leo_gateway v0.12.5](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.12.5](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.12.5](https://github.com/leo-project/leo_storage.git)
        * [ecache v0.10.2](https://github.com/leo-project/ecache.git)
        * [cherly v0.10.1](https://github.com/leo-project/cherly.git)
    * others
        * [bitcask](https://github.com/basho/bitcask.git)
        * [cowboy v0.6.2](https://github.com/leo-project/cowboy.git) - forked from [extend/cowboy](https://github.com/extend/cowboy)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlang-lz4)


0.12.3 (Nov 9, 2012)
--------------------

* Improve performances
    * Storage Performance Tuning#3
        * Reduced using list_to_binary/1 - [leo_storage, leo_object_storage]
        * Unified internal storage data-type to "binary"
* Improve S3 compatibility
    * Support Multipart upload an object (large-object)
* New feature
    * Able to monitor (SNMP)
        * Sum of objects/storage-node
        * Sum of object-length/storage-node
* Fix bugs
    * Deletion of chunked objects (large-object)
    * Fail rebalance when exists a restarting node
        * Adjust the start timing of RPC for reject requests from remote-node(s)

* Used libraries
    * leo project
        * [leo_commons v0.12.5](https://github.com/leo-project/leo_commons.git)
        * [leo_backend-db v0.10.8](https://github.com/leo-project/leo_backend_db.git)
        * [leo_object_storage v0.12.10](https://github.com/leo-project/leo_object_storage.git)
        * [leo_mq v0.10.5](https://github.com/leo-project/leo_mq.git)
        * [leo_ordning_reda v0.8.3](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v0.12.0](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.10.6](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.10.5](https://github.com/leo-project/leo_statistics.git)
        * [leo_logger v0.10.1](https://github.com/leo-project/leo_logger.git)
        * [leo_gateway v0.12.4](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.12.4](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.12.4](https://github.com/leo-project/leo_storage.git)
        * [ecache v0.10.1](https://github.com/leo-project/ecache.git)
        * [cherly v0.10.0](https://github.com/leo-project/cherly.git)
    * others
        * [bitcask](https://github.com/basho/bitcask.git)
        * [cowboy v0.6.2](https://github.com/leo-project/cowboy.git) - forked from [extend/cowboy](https://github.com/extend/cowboy)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlang-lz4)


0.12.2 (Nov 2, 2012)
--------------------

* Improve performances
    * Storage Performance Tuning#2
        * Revised put operation
* Improve S3 compatibility
    * Support deletion of a bucket
    * Support [s3cmd](http://s3tools.org/s3cmd) (s3-client)
* Fix bugs
    * Gateway:
        * NOT able to store object-cache because data-type is replaced from string to binary with 0.12.1
    * Storage "Compaction"
        * When excuting compact-command, Objects to be removed remain (chunked objects)
* Used libraries
    * leo project
        * [leo_commons v0.12.3](https://github.com/leo-project/leo_commons.git)
        * [leo_backend-db v0.10.7](https://github.com/leo-project/leo_backend_db.git)
        * [leo_object_storage v0.12.9](https://github.com/leo-project/leo_object_storage.git)
        * [leo_mq v0.10.4](https://github.com/leo-project/leo_mq.git)
        * [leo_ordning_reda v0.8.2](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v0.10.4](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.10.5](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.10.4](https://github.com/leo-project/leo_statistics.git)
        * [leo_logger v0.10.0](https://github.com/leo-project/leo_logger.git)
        * [leo_gateway v0.12.3](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.12.3](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.12.3](https://github.com/leo-project/leo_storage.git)
        * [ecache v0.10.1](https://github.com/leo-project/ecache.git)
        * [cherly v0.10.0](https://github.com/leo-project/cherly.git)
    * others
        * [bitcask](https://github.com/basho/bitcask.git)
        * [cowboy v0.6.2](https://github.com/leo-project/cowboy.git) - forked from [extend/cowboy](https://github.com/extend/cowboy)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlang-lz4)


0.12.1  (Oct 25, 2012)
----------------------

* Improve performances
    * Storage Performance Tuning#1
        * Reduced overhead
            * Modified replicator/repairer from gen_server to module
            * Revised data-flow from storage-engine to object/metadata storage
    * Reduced using list_to_binary/1
        * Modified bucket-related libs: [leo_gateway,leo_manager,leo_s3_libs]
    * Compressor/Decompressor replace from snappy to lz4
* Fix bugs
    * Has omissions an object of rebalance
    * Fixed S3 releated:
        * NOT able to remove an endpoint
        * Able to add a bucket with NOT exists access-key

* Used libraries
    * leo project
        * [leo_commons v0.12.0](https://github.com/leo-project/leo_commons.git)
        * [leo_backend-db v0.10.4](https://github.com/leo-project/leo_backend_db.git)
        * [leo_object_storage v0.12.4](https://github.com/leo-project/leo_object_storage.git)
        * [leo_mq v0.10.2](https://github.com/leo-project/leo_mq.git)
        * [leo_ordning_reda v0.8.0](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v0.10.2](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.10.3](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.10.2](https://github.com/leo-project/leo_statistics.git)
        * [leo_logger v0.9.8](https://github.com/leo-project/leo_logger.git)
        * [leo_gateway v0.12.1](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.12.2](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.12.1](https://github.com/leo-project/leo_storage.git)
        * [ecache v0.10.1](https://github.com/leo-project/ecache.git)
        * [cherly v0.10.0](https://github.com/leo-project/cherly.git)
    * others
        * [bitcask](https://github.com/basho/bitcask.git)
        * [cowboy v0.6.2](https://github.com/leo-project/cowboy.git) - forked from [extend/cowboy](https://github.com/extend/cowboy)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlang-lz4)


0.12.0 (Oct 20, 2012)
----------------------

* New feature - Large Object Support
    * Handled from a few bytes an object to a few GB an object
* Improve performances
    * Gateway Performance Tuning
        * HTTP-Server replace from Mochiweb to Cowboy
        * Reduced using list_to_binary/1
    * Revised order of system launch
        * before: Managers -> Storage -> Gateway
        * after : Managers -> Storage|Gateway
    * Changed type of key from string to binary
* Fix bugs
    * S3-API related
        * Overwrited bucket-info by NOT owners
        * When put-operation, NOT returned 'ETag' header
    * Compaction
        * When excuting compact-command, Objects to be removed partly may remain
* Used libraries
    * leo project
        * [leo_commons v0.12.0](https://github.com/leo-project/leo_commons.git)
        * [leo_backend-db v0.10.4](https://github.com/leo-project/leo_backend_db.git)
        * [leo_object_storage v0.12.3](https://github.com/leo-project/leo_object_storage.git)
        * [leo_mq v0.10.2](https://github.com/leo-project/leo_mq.git)
        * [leo_ordning_reda v0.6.1](https://github.com/leo-project/leo_ordning_reda.git)
        * [leo_redundant_manager v0.10.2](https://github.com/leo-project/leo_redundant_manager.git)
        * [leo_s3_libs v0.10.2](https://github.com/leo-project/leo_s3_libs.git)
        * [leo_statistics v0.10.1](https://github.com/leo-project/leo_statistics.git)
        * [leo_logger v0.9.7](https://github.com/leo-project/leo_logger.git)
        * [leo_gateway v0.12.0](https://github.com/leo-project/leo_gateway.git)
        * [leo_manager v0.12.0](https://github.com/leo-project/leo_manager.git)
        * [leo_storage v0.12.0](https://github.com/leo-project/leo_storage.git)
        * [ecache v0.10.1](https://github.com/leo-project/ecache.git)
        * [cherly v0.10.0](https://github.com/leo-project/cherly.git)
    * others
        * [bitcask](https://github.com/basho/bitcask.git)
        * [cowboy v0.6.2](https://github.com/leo-project/cowboy.git) - forked from [extend/cowboy](https://github.com/extend/cowboy)
        * [folsom](https://github.com/boundary/folsom.git)
        * [jiffy](https://github.com/davisp/jiffy.git)
        * [lz4 v0.1.1](https://github.com/leo-project/erlang-lz4.git) - forked from [szktty/erlang-lz4](https://github.com/szktty/erlang-lz4)
        * [snappy](https://github.com/fdmanana/snappy-erlang-nif.git)


0.10.2 (Sep 25, 2012)
----------------------

* Improve performances
    * NOT used "proplists:get_value" function
        * Replace from "proplists:get_value/2,3" to "lists:keyfind/2"
    * Related libs:
        * leo_gateway
        * leo_storage
        * leo_manager
        * leo_logger
        * leo_mq
        * leo_object_storage
        * leo_ordning_reda
        * leo_redundant_manager
        * leo_s3_libs
        * leo_statistics
* Improve leo_manager
    * Support output of json-format
    * Support multi-ports TCP-server
        * for CUI console
        * for Application (JSON-Format)
* Improve leo_storage
    * Support plural devices
    * Reduced rebalance/recover costs
        * Support compression of stacked objects and decompresson of received objects (Using snappy)
* Fix bugs
    * leo-gateway related (S3-related):
        * Create bucket from 'Dragon Disk'
        * When using cowboy can send bad values(not iodata)


0.10.1 (Sep 12, 2012)
---------------------

* Improve leo_hex performances
    * "binary_to_hex" function
    * Related libs:
        * leo_gateway
        * leo_object_storage
        * leo_redundant_manager
    * By this correspondence, LeoFS's performance improved 20% up.
* Improve leo_manager
    * Format of output from manager-console
        * Commands:
            * "status"
            * "whereis"
* Improve performance of "storage-stats" in manager-console
* Fix bugs
    * A handling error in S3-libs


0.10.0 (Aug 30, 2012)
---------------------

* Improve S3-API's compatibility
    * Add S3-authentication
    * Add S3-bucket
* Add S3-related command in LeoFS's manager
    * "s3-gen-key" : Generate a S3 key pair(AccessKeyID and SecretAccessKey)
    * "s3-set-endpoint" : Register a new S3 Endpoint
    * "s3-delete-endpoint" : Delete a S3 Endpoint
    * "s3-get-endpoints" : Retrieve all of S3 Endpoints registered
    * "s3-get-buckets" : Retrieve all of Buckets registered
* Improve order of system launch
    * Remove "attach command" in manager - After Storage launched, the node's state is automatically changed to "attached"
* Improve rebalance-function's performance which is about 5 times compare with v0.9.1
* Improve compact-function. Restrain storage's load when compact objects.
* Fix bugs
    * Deletion of Zero bytes in Storage
    * Behavior after the restart of Manager
    * Re-register procs into the Manager's monitor


0.9.1 (Jul 13, 2012)
--------------------

* Remove "apps" directory in leofs - Modified "reltool.config"
* Fix 'shadow vars'
* Remove ZMQ log-appender and AMQP log-appender for leo_logger, They will be provided LeoFS's sub projects.
* Improve - In order to be able to extend "LeoFS's Object Container's file format".


0.9.0  (Jul 4, 2012)
--------------------

* Initial release
