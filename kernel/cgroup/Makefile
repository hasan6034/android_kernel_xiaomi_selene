# SPDX-License-Identifier: GPL-2.0

ifeq ($(cc-name),clang)
ifdef CONFIG_INLINE_OPTIMIZATION
ccflags-y += -mllvm -inline-threshold=15000
ccflags-y += -mllvm -inlinehint-threshold=10000
endif
endif

obj-y := cgroup.o namespace.o cgroup-v1.o

obj-$(CONFIG_CGROUP_FREEZER) += freezer.o
obj-$(CONFIG_CGROUP_PIDS) += pids.o
obj-$(CONFIG_CGROUP_RDMA) += rdma.o
obj-$(CONFIG_CPUSETS) += cpuset.o
obj-$(CONFIG_CGROUP_DEBUG) += debug.o
