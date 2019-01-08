# score-keeper-project
an Udacity project
Below is the copy of the code in Java:

package com.example.android.courtcounter;

import android.os.Bundle;
import android.support.v7.app.AppCompatActivity;
import android.view.View;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    int scoreReds = 0;
    int scoreBlues = 0;
    int foulsReds = 0;
    int foulsBlues = 0;


    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

    }

    /**

     * Displays the given score for Reds.

     */

    public void displayForReds(int score) {

        TextView scoreView = (TextView) findViewById(R.id.reds_score);

        scoreView.setText(String.valueOf(score));

    }

    public void displayFoulsReds(int score) {

        TextView scoreView = (TextView) findViewById(R.id.fouls_reds);

        scoreView.setText(String.valueOf(score));

    }

    /**

     * Displays the given score for Blues.

     */

    public void displayForBlues(int score) {

        TextView scoreView = (TextView) findViewById(R.id.blues_score);

        scoreView.setText(String.valueOf(score));

    }

    public void displayFoulsBlues(int score) {

        TextView scoreView = (TextView) findViewById(R.id.fouls_blues);

        scoreView.setText(String.valueOf(score));

    }

    /**
     * displays method for reseting the score back to zero
     */

    public void resetScore (View view) {
        scoreReds = 0;
        scoreBlues = 0;
        foulsReds = 0;
        foulsBlues = 0;
        displayForReds(scoreReds);
        displayForBlues(scoreBlues);
        displayFoulsReds(foulsReds);
        displayFoulsBlues(foulsBlues);
    }

    /**

     * increases the score by one point

     */

    public void addGoalsReds(View view) {
        scoreReds = scoreReds + 1;
        displayForReds(scoreReds);
    }

    public void addFoulsReds(View view) {
        foulsReds = foulsReds + 1;
        displayFoulsReds(foulsReds);
    }


    /**

     * increases the score by one point

     */

    public void addGoalsBlues(View view) {
        scoreBlues = scoreBlues + 1;
        displayForBlues(scoreBlues);
    }

    public void addFoulsBlues(View view) {
        foulsBlues = foulsBlues + 1;
        displayFoulsBlues(foulsBlues);
    }


}
