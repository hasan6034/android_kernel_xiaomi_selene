# SPDX-License-Identifier: GPL-2.0

ifeq ($(cc-name),clang)
ifdef CONFIG_INLINE_OPTIMIZATION
ccflags-y += -mllvm -inline-threshold=15000
ccflags-y += -mllvm -inlinehint-threshold=10000
endif
endif

obj-y := irqdesc.o handle.o manage.o spurious.o resend.o chip.o dummychip.o devres.o
obj-$(CONFIG_IRQ_TIMINGS) += timings.o
obj-$(CONFIG_GENERIC_IRQ_CHIP) += generic-chip.o
obj-$(CONFIG_GENERIC_IRQ_PROBE) += autoprobe.o
obj-$(CONFIG_IRQ_DOMAIN) += irqdomain.o
obj-$(CONFIG_IRQ_SIM) += irq_sim.o
obj-$(CONFIG_PROC_FS) += proc.o
obj-$(CONFIG_GENERIC_PENDING_IRQ) += migration.o
obj-$(CONFIG_GENERIC_IRQ_MIGRATION) += cpuhotplug.o
obj-$(CONFIG_PM_SLEEP) += pm.o
obj-$(CONFIG_GENERIC_MSI_IRQ) += msi.o
obj-$(CONFIG_GENERIC_IRQ_IPI) += ipi.o
obj-$(CONFIG_SMP) += affinity.o
obj-$(CONFIG_GENERIC_IRQ_DEBUGFS) += debugfs.o
