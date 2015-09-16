# python
This is the Class Project . CS 521

def bmi_calculation():
  quit = False
  count = 0

  print('Welcome to the Project')
  print('Enter your Name')
  name=input();
  print('Hi', name)
  value = input('\nEnter "q" to quit or any letter to continue')
  if value == 'q':
   quit = True


  while (not quit and count < 10):

      weight = float(input('Enter weight in pounds: '))
      height = float(input('Enter height in inches: '))

# Weight cannot be less than 0 or greater than 500
      if weight <= 0 or weight > 500:
          print ('Weight cannot be less than 0 or greater than 500')
          continue

# Height cannot less than or equal to 0 inches
      elif height <= 0:
          print ('Height cannot be less than 0')
          continue

      else:
          bmi = (weight / (height * height)) * 703.0
          print ('Your BMI is %.2f' % bmi)
          if bmi <= 18.5:
              print ('Your weight status is Underweight')
          elif bmi >= 18.5 and bmi <= 24.9:
              print ('Your weight status is Normal weight')
          elif bmi >= 25 and bmi <= 29.9:
              print ('Your weight status is Overweight')
          elif bmi >= 30:
              print ('Your weight status is Obese')


      count = count + 1
      if count < 10:
        value = input('\nEnter "q" to quit, or any letter to continue ')
        if value == 'q':
            quit = True

bmi_calculation()
input('\n  Press <enter> to exit')
