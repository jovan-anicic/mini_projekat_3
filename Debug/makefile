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
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
tastatura.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
tastatura.list \

OBJCOPY_HEX += \
tastatura.hex \

OBJCOPY_BIN += \
tastatura.bin \


# All Target
all: tastatura.elf secondary-outputs

# Tool invocations
tastatura.elf: $(OBJS) $(USER_OBJS) D:\4.\ godina\Prvi\ semestar\Mikroprocesorski\ sistemi\moji_cube_ide\tastatura\STM32F103C6TX_FLASH.ld
	arm-none-eabi-gcc -o "tastatura.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"D:\4. godina\Prvi semestar\Mikroprocesorski sistemi\moji_cube_ide\tastatura\STM32F103C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="tastatura.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

tastatura.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "tastatura.list"
	@echo 'Finished building: $@'
	@echo ' '

tastatura.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "tastatura.hex"
	@echo 'Finished building: $@'
	@echo ' '

tastatura.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "tastatura.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
