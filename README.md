# Weather-APP
Isaac Quentin SANDZOU
ST10458715

Exam IMAD
package com.example.myapplicationforecoastapplicationexam

import android.content.Intent
import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.widget.Button

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)



        val startButton = findViewById<Button>(R.id.startButton)
        val exitButton = findViewById<Button>(R.id.exitButton)



        startButton.setOnClickListener {

            //Start activity when start Button is clicked
            startActivity(Intent(this, MainActivity2::class.java))

        }
        //Exit the app when exit Button is clicked
        exitButton.setOnClickListener {
            finish()
        }
    }
}

package com.example.myapplicationforecoastapplicationexam

import android.content.Intent
import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView

class MainActivity2 : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main2)



        val generateButton = findViewById<Button>(R.id.generateButton)
         val viewDetailsButton = findViewById<Button>(R.id.viewDetailsButton)
         val clearButton = findViewById<Button>(R.id.clearButton)
         val exitButton2 = findViewById<Button>(R.id.exitButton2)
         val averageEditText = findViewById<EditText>(R.id.averageEditText)
         val dayOfWeek = arrayOf("Monday","Tuesday","Wednesday","Thursday", "Friday", "Saturday", "Sunday")
         val temperaturesMin = arrayOf("23", "18", "12","15","11","18","15")
         val temperaturesMax = arrayOf("6","3","2","9","4","8","1")
        val resultAvearageOfTheWeek = findViewById<TextView>(R.id.resultAvearageOfTheWeek)
        viewDetailsButton.setOnClickListener {
            //Start activity 3 when view details Button is clicked
            startActivity(Intent(this, MainActivity4::class.java))

            generateButton.setOnClickListener {

                // Declaration of the userInput variable to store user input
                val userInput = averageEditText.text.toString()

            exitButton2.setOnClickListener {
                finish()

                clearButton.setOnClickListener {
                    averageEditText.text.clear()

                    val userInput = averageEditText.text.toString()

                    if (userInput.isEmpty()) {
                        resultAvearageOfTheWeek.text = "Please enter the day of the week"

                    } else {
                        // Convert the user input to an integer or null if the input is not a valid number
                        val averageEditText = userInput.toIntOrNull()

                        val result = when (averageEditText) {

                            1 -> "The weather average of the week is a min of 16C AND a of max is 5C"
                            else -> "There is only the average of a week available, put 1 for a week"

                        }
                    }
                }
            }

        }
    }

}}

package com.example.myapplicationforecoastapplicationexam

import android.content.Intent
import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView

class MainActivity4 : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main4)



                val generateButton = findViewById<Button>(R.id.generateButton)
                val dayOfWeek = arrayOf("Monday","Tuesday","Wednesday","Thursday", "Friday", "Saturday", "Sunday")
                val temperaturesMin = arrayOf("23", "18", "12","15","11","18","15")
                val temperaturesMax = arrayOf("6","3","2","9","4","8","1")
                val userDay = findViewById<EditText>(R.id.userDay)
                val backButton = findViewById<Button>(R.id.backButton)
                val resultDayTemperature = findViewById<TextView>(R.id.resultDayTemperature)


        generateButton.setOnClickListener {

            // Declaration of the userInput variable to store user input
            val userInput = userDay.text.toString()


                    backButton.setOnClickListener {
                    val intent = Intent(this, MainActivity::class.java)
                    startActivity(intent)

                    val userInput = userDay.text.toString()

                    if (userInput.isEmpty()) {
                        resultDayTemperature.text = "Please enter the day of the week"

                    } else {
                        // Convert the user input to an integer or null if the input is not a valid number
                        val userDay = userInput.toIntOrNull()

                        val result = when (userDay) {

                            1 -> "Monday, the minimum temperature is 23C, and the maximum temperature is 6C"
                            2 -> "Tuesday, the minimum temperature is 18C, and the maximum is temperature is 3C"
                            3 -> "Wednesday, the minimum temperature is 12C, and the maximum temperature is 2C"
                            4 -> "Thursday, the minimum temperature is 15C, and the maximum temperature is 9C"
                            5 -> "Friday, the minimum temperature is 11C, and the maximum temperature is 4C"
                            6 -> "Saturday, the minimum temperature is 18C, and the maximum temperature is 8C"
                            7 -> "Sunday, the minimum temperature is 15C, and the maximum temperature is 1C"
                            else -> "There is 7 days in the week, put a number between 1 and 7. 1 is for Monday and 7 for Sunday"

                        }

                    }

                }

            }
        }



    }

Link GitHub repository
https://github.com/Isaacquentin/Weather-APP/blob/main/README.md

Splash Screen (First Screen)
The splash Screen we have designed is truly tailored to provide a universal and engaging welcome experience. The colors have been meticulously chosen for their visual appeal while ensuring optimal readability across all devices. Additionally, the information is strategically arranged to be easily identifiable and visible at first glance. 
We have taken great care to ensure that every aspect of the Splash Screen is perfectly suited to all viewers, regardless of their device or visual preferences, ensuring a seamless and enjoyable user experience right from the start.
![image](https://github.com/Isaacquentin/Weather-APP/assets/166740424/91a75251-016c-4575-a58d-019ab2c129c0)


MAIN SCREEN
Our Main Screen has been meticulously crafted with the user in mind, providing a visually appealing and intuitive interface to quickly access essential weather information. As soon as  the user opens the application, they are greeted with a clear and concise overview of the weather, coupled with easily accessible navigation options.
Each element on the  main screen is thoughtfully organized to facilitate seamless navigation through various sections to check the weather forecast for the week. By inputting required information.
![Screenshot 2024-06-10 133026](https://github.com/Isaacquentin/Weather-APP/assets/166740424/0c36e137-0b3f-4e52-bd16-c16de390439d)





