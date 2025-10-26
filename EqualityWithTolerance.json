// автор кода: vk121230
// код написан одной песней (3 минуточек)
(function(Scratch) {
  'use strict';

  class EqualityWithTolerance {
    getInfo() {
      return {
        id: 'equalityWithTolerance', // Это типо ID моего расширения
        name: 'Сравнение с погрешностью',
        // --- НОВЫЕ ЦВЕТА ---
        color1: '#59C059', // Основной цвет блока (fill)
        color2: '#389438', // Цвет полей ввода и обводки (stroke)
        color3: '#2E7D2E', // Самый темный цвет для меню
        // --------------------
        blocks: [
          {
            opcode: 'areNumbersEqualWithTolerance',
            blockType: Scratch.BlockType.BOOLEAN, // Это и есть логический блок
            text: '[NUM1] = [NUM2] с допустимой погрешностью [TOLERANCE]',
            arguments: {
              NUM1: {
                type: Scratch.ArgumentType.NUMBER,
                defaultValue: 1
              },
              NUM2: {
                type: Scratch.ArgumentType.NUMBER,
                defaultValue: 3
              },
              TOLERANCE: {
                type: Scratch.ArgumentType.NUMBER,
                defaultValue: 2
              }
            }
          }
        ]
      };
    }

    areNumbersEqualWithTolerance(args) {
      // Тут лучше использовать Scratch.Cast ну для надежного преобразования в числа
      const num1 = Scratch.Cast.toNumber(args.NUM1);
      const num2 = Scratch.Cast.toNumber(args.NUM2);
      const tolerance = Scratch.Cast.toNumber(args.TOLERANCE);

      // Вычисляем тут абсолютную разницу
      const difference = Math.abs(num1 - num2);

      // А теперь выравниваем разницу с допустимой погрешностью
      return difference <= tolerance;
    }
  }

  // Делаем штоб импортировалось (не трохай)
  Scratch.extensions.register(new EqualityWithTolerance());
})(Scratch);
