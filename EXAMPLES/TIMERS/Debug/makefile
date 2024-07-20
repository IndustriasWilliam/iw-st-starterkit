################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (11.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/MemMang/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM0/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/subdir.mk
-include Drivers/STM32F0xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := iW - ST Starter Kit
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
iW\ -\ ST\ Starter\ Kit.elf \

MAP_FILES += \
iW\ -\ ST\ Starter\ Kit.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
iW\ -\ ST\ Starter\ Kit.list \

OBJCOPY_HEX += \
iW\ -\ ST\ Starter\ Kit.hex \

OBJCOPY_BIN += \
iW\ -\ ST\ Starter\ Kit.bin \


# All Target
all: main-build

# Main-build Target
main-build: iW\ -\ ST\ Starter\ Kit.elf secondary-outputs

# Tool invocations
iW\ -\ ST\ Starter\ Kit.elf iW\ -\ ST\ Starter\ Kit.map: $(OBJS) $(USER_OBJS) C:\Users\lorra\Documents\industrias-william\iW-Little\EXAMPLES-CODE\STM32F030F4PX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "iW - ST Starter Kit.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0 -T"C:\Users\lorra\Documents\industrias-william\iW-Little\EXAMPLES-CODE\STM32F030F4PX_FLASH.ld" --specs=nosys.specs -Wl,-Map="iW - ST Starter Kit.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

iW\ -\ ST\ Starter\ Kit.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "iW - ST Starter Kit.list"
	@echo 'Finished building: $@'
	@echo ' '

iW\ -\ ST\ Starter\ Kit.hex: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "iW - ST Starter Kit.hex"
	@echo 'Finished building: $@'
	@echo ' '

iW\ -\ ST\ Starter\ Kit.bin: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "iW - ST Starter Kit.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) default.size.stdout iW\ -\ ST\ Starter\ Kit.bin iW\ -\ ST\ Starter\ Kit.elf iW\ -\ ST\ Starter\ Kit.hex iW\ -\ ST\ Starter\ Kit.list iW\ -\ ST\ Starter\ Kit.map iW\\ -\\ ST\\ Starter\\ Kit.elf
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
