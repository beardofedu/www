:template: 2016/eu.html

{% set dont_link = ['Lunch',
                    'Intro',
                    'Group Photo',
                    'Snack break',
                    'Switch Speakers',
                    'Doors Open, Breakfast Served',
                    'Introduction & State of the Docs',
                    'Lightning Talks',
                    'Day 1 wraps up',
                    'Closing & Group Photo',
                    'Day 2 wraps up'] %}

Schedule
========

Write the Docs is more than a conference. Each year we organize a wide
range of events so that people can come together, collaborate, and learn
from each other in different ways.

Saturday, September 17th
------------------------
If you're in town early, we'll organize some sight-seeing activities to introduce
you to this lovely city and to meet other documentarians who will be around.

.. raw:: html

   <table class="schedule">
   <tr>
    <td class="schedule-time">13:45</td>
    <td>Boarding at <a href="https://goo.gl/maps/bqLP3VaytVo">Prague Boats, pier no. 5 of Dvořákovo nábřeží<a/></td>
   </tr>
   <tr>
    <td class="schedule-time">16:00</td>
    <td>Return to the docs</td>
   </tr>
   </table>


Sunday, September 18th
----------------------

During the day, we’ll hold our :doc:`Writing Day documentation
sprints </conf/eu/2016/writingday>` at the same venue as the rest of the conference, followed by the conference reception in the evening.
We encourage everyone to drop by on Sunday evening for the conference reception.

You’ll have a chance to get acquainted with each other over some drinks and snacks.
We’ll also help groups organize dinner plans, so you can continue your conversations
over more substantial food as well.


.. raw:: html

   <table class="schedule">
   <tr>
    <td class="schedule-time">09:00</td>
    <td>Breakfast
   </tr>
   <tr>
    <td class="schedule-time">10:00</td>
    <td><a href="/conf/eu/2016/writingday/">Writing Day</a> documentation sprints begin</td>
   </tr>
   <tr>
    <td class="schedule-time">10:30</td>
    <td>Introduction to the Writing Day</td>
   </tr>
   <tr>
    <td class="schedule-time">13:00</td>
    <td>Lunch
   </tr>
   <tr>
    <td class="schedule-time">17:00</td>
    <td>Writing Day ends. Reception begins. Stop working and start chatting! Snacks and drinks provided.</td>
   </tr>
   <tr>
    <td class="schedule-time">19:00</td>
    <td>Reception ends</td>
   </tr>
   </table>


Monday, September 19th - Day 1
------------------------------

This is the main event! Hear from lots of interesting folks about all
things documentation.

Parallel to the main presentations, we will also provide an unconference space
each afternoon as well as lightning talks. Sign up for these on the morning of
the event.

Main Stage
~~~~~~~~~~

.. raw:: html

    <table>
    {% for talk in eu_2016_day1 %}
      <tr>
        <td class=" schedule-time">{{ talk.Time }}</td>
        <td>

        {% if talk.Session in dont_link %}

        {{ talk.Session}}

        {% else %}

`{{ talk.Session }} </conf/na/2016/speakers/#speaker-{{ talk.slug }}>`_

.. raw:: html

        {% endif %}


        </td>
      </tr>

    {% endfor %}
    </table>

Unconference
~~~~~~~~~~~~

:doc:`/conf/eu/2016/unconference` from 13:00-17:00

Monday Night - Party
~~~~~~~~~~~~~~~~~~~~

The party will be at `Klub Lavka, Novotného lávka 201/1 <https://goo.gl/maps/3k5XZQvkHZr>`_ from **19:00-23:00**.

Wind down and talk about the day's talks in a relaxed and friendly
environment. Free drinks of all varieties, snacks, and sweets will be
provided.


Tuesday, September 20th - Day 2
-------------------------------

More interesting folks, more things documentation. Unconference space and
lightning talks too!

Main Stage
~~~~~~~~~~

.. raw:: html

    <table>
    {% for talk in eu_2016_day2 %}
      <tr>
        <td class=" schedule-time">{{ talk.Time }}</td>
        <td>

        {% if talk.Session in dont_link %}

        {{ talk.Session}}

        {% else %}

`{{ talk.Session }} </conf/na/2016/speakers/#speaker-{{ talk.slug }}>`_

.. raw:: html

        {% endif %}


        </td>
      </tr>

    {% endfor %}
    </table>

Unconference
~~~~~~~~~~~~

:doc:`/conf/eu/2016/unconference` from 13:00-17:00
