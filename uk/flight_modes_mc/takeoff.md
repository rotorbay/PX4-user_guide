# Режим зльоту (Мультикоптер)

<img src="../../assets/site/position_fixed.svg" title="Position fix required (e.g. GPS)" width="30px" />

У режимі польоту _Зліт_ транспортний засіб піднімається на задану висоту і чекає на подальші вказівки.

:::info

- Режим є автоматичним - для керування транспортним засобом не потрібне _втручання_ користувача.
- Режим потребує принаймні дійсної локальної оцінки позиції (не потребує глобальної позиції).
  - Літаючі апарати не можуть перемикатися в цей режим без дійсної локальної позиції.
  - Літаючі транспортні засоби перейдуть в режим аварійної безпеки, якщо втратять оцінку положення.
  - Роззброєні транспортні засоби можуть переключатися в режим без дійсної оцінки позиції, але не можуть озброюватися.
- Перемикачі керування RC можна використовувати для зміни режимів польоту.
- Рух палиць дистанційного керування [за замовчуванням](#COM_RC_OVERRIDE) змінить транспортний засіб на [режим позиції](../flight_modes_mc/position.md), якщо не буде обробки критичного відключення батареї.
- [Детектор несправностей](../config/safety.md#failure-detector) автоматично зупинить мотори, якщо на зльоті виникне проблема.

<!-- https://github.com/PX4/PX4-Autopilot/blob/main/src/modules/commander/ModeUtil/mode_requirements.cpp -->

:::

## Технічний підсумок

Багатовертольот вибуває вертикально на висоту, визначену в [MIS_TAKEOFF_ALT](../advanced_config/parameter_reference.md#MIS_TAKEOFF_ALT) і утримує позицію.

Рух палиці RC змінить транспортний засіб на [Режим положення](../flight_modes_mc/position.md) (за [за замовчуванням](#COM_RC_OVERRIDE)).

### Параметри

Взліт впливається наступними параметрами:

| Параметр                                                                                                | Опис                                                                                                                                                                                                                                                                                       |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <a id="MIS_TAKEOFF_ALT"></a>[MIS_TAKEOFF_ALT](../advanced_config/parameter_reference.md#MIS_TAKEOFF_ALT) | Цільова висота під час злітання (типово: 2.5м)                                                                                                                                                                                                                                             |
| <a id="MPC_TKO_SPEED"></a>[MPC_TKO_SPEED](../advanced_config/parameter_reference.md#MPC_TKO_SPEED)     | Швидкість підйому (за замовчуванням: 1.5м/с)                                                                                                                                                                                                                                               |
| <a id="COM_RC_OVERRIDE"></a>[COM_RC_OVERRIDE](../advanced_config/parameter_reference.md#COM_RC_OVERRIDE) | Контролює переміщення джойстика на мультикоптері (або конвертоплані у режимі MC) зміну режиму на [Режим положення](../flight_modes_mc/position.md). Це можна окремо увімкнути для автоматичних режимів та для режиму поза бортом, і в автоматичних режимах воно включено за замовчуванням. |
| <a id="COM_RC_STICK_OV"></a>[COM_RC_STICK_OV](../advanced_config/parameter_reference.md#COM_RC_STICK_OV) | Кількість рухів стиків, яка викликає перехід у режим [Положення](../flight_modes_mc/position.md) (якщо [COM_RC_OVERRIDE](#COM_RC_OVERRIDE) увімкнено)                                                                                                                                    |

## Дивись також

- [Запуск з катапульти чи підкиданням (MC)](../flight_modes_mc/throw_launch.md)
- [Злітній режим (FW)](../flight_modes_fw/takeoff.md)

<!-- this maps to AUTO_TAKEOFF in dev -->
