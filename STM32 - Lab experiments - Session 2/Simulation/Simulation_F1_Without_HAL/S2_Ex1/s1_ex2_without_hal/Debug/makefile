################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
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

BUILD_ARTIFACT_NAME := s1_ex2_without_hal
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX := 
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME).$(BUILD_ARTIFACT_EXTENSION)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
s1_ex2_without_hal.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
s1_ex2_without_hal.list \

OBJCOPY_HEX += \
s1_ex2_without_hal.hex \

OBJCOPY_BIN += \
s1_ex2_without_hal.bin \


# All Target
all: main-build

# Main-build Target
main-build: s1_ex2_without_hal.elf secondary-outputs

# Tool invocations
s1_ex2_without_hal.elf: $(OBJS) $(USER_OBJS) C:\ST\STM32CubeIDE_1.5.1\s1_ex2_without_hal\STM32F103C4TX_FLASH.ld
	arm-none-eabi-gcc -o "s1_ex2_without_hal.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\ST\STM32CubeIDE_1.5.1\s1_ex2_without_hal\STM32F103C4TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="s1_ex2_without_hal.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

s1_ex2_without_hal.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "s1_ex2_without_hal.list"
	@echo 'Finished building: $@'
	@echo ' '

s1_ex2_without_hal.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "s1_ex2_without_hal.hex"
	@echo 'Finished building: $@'
	@echo ' '

s1_ex2_without_hal.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "s1_ex2_without_hal.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents fail-specified-linker-script-missing warn-no-linker-script-specified
.SECONDARY:

-include ../makefile.targets
