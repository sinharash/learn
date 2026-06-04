So it's the cluster soul 90, the database name, the global cluster endpoint, and the primary cluster identifier.

And you just create a new app service.

With those things as well as...

It's just those things, and then the type, in DMS, and that's it.

Good.

Boop, boop, boop.

Give me a second.

Thank you so much.

Is this in project, or is it in test, or what environment do you do?

In my branch right now.

Okay.

And Rashby's pointing into that under Earth, local bridge.

Okay.

And if you want, I can share my screen.

Sure, and show you, uh, vacation for it.

Just get a toke and get it up.

You took it, man.

You should keep going now.

So, you know, when that comes through.

Okay.

Okay, yeah, so...

It's pretty straightforward.

Okay.

Cool.

Uh, and then they're gonna pass something extra back on the geeta base entry.

So we have to call, like, get business application for DMS explicitly.

Explicitly?

Yeah.

Okay.

And then, like, the only thing they're.. That matters.

Is this single output here?

This is the only thing that needs to be displayed.

God, I am.

Okay.

I mean, just check our DBs real quick, see if we have an example one.

Okay, so now you were all the output on the DV, right?

Itself?

Yeah, what you call it?

DMS is enabled, here's the UR, I'll go to it.

Mm.

I mean, cool.

Uh, let me just make sure we have the cluster name.

Or the Cluster Soma?

Don't know if we have that.

I don't think we really even know anything about the cluster, 'cause I think we give you the DB and then you guys find the cluster.

Oh, we got clustered name.

Oh, we do, of course, there's so many.

Sweet.

Okay.

And then what were the other ones?

Uh?

A database, Sydney, Houston, can we got that?

A little bit closer end point.

We have the, okay, we got, yeah, so we got all of it.

So, the restaurant, you just...

Some, somewhere on the UI, in the database.

This is just me having, like, a 10 minute understanding of how this works.

Uh, you're gonna call to get the application service for the DMS, if it's not enabled.

I'm not sure Is there only specific people that are allowed to enable this?

I remember there was, like, some exception process being talked about.

Um...

I think that all went away.

Okay, so anybody from any database can enable us?

I don't see anything in the requirements.

Yeah.

Cool.

So we'll just go with that then.

Uh...

So, yeah, you will check, and you will call it application service, uh, Deemas, and if it returns nothing, what does your application service, uh, query look like?

Can you go back to that?

It's fun.

Yeah.

And then you just pass it...

Okay, so it's named as Newton DMS.

Okay, so I'm assuming the naming convention...

If we call, there's nothing on the call to the database query, then we'll return that, right?

Unless...

Or is that the name of your database?

Yeah, so, like, this is here.

Oh, God, this is quick.

You're calling just to get the database, right?

It's this.

Mm.

And the DMS is just on there.

Now, I mean, to something real quick that I haven't tested before.

I don't put anything on the DB itself, saying that it's been enabled.

Unfortunately, no, because sick, or that they're separate surface catalog runs.

St stupid.

All right.

Yeah.

All right, so you're just gonna have to go by naming convention, Rashmi?

Uh, assuming that's how they create all their DNS things, is just adding that to the end of the database name.

Okay.

You'll have to, essentially, Yes, you'll do this, dash.

So that'll return the database, but then...

And then I want to test this real quick, like, if there's knocking for this one...

Okay, so...

Yeah.

Okay, so, it's gonna be kind of weird, and it may or may not, I'm gonna be clunky, but you're gonna need to basically run this query, check if they have a DMS resource.

If they don't, then maybe that's where you can have them, like, select, like, turn on or something.

And then when they turn it on, it'll act just like any other thing.

It will go...

And until that endpoint refreshes, I don't know what it looks like when you first submit it, doesn't go into, like, Is there a status of the mutation, like, provisioning or something?

Does it work like the rest of them?

Yep, it's the same.

So, if you call that and you get a status of provisioning, then you know it's in the process of turning on.

And then when it's turned on, then you just have the URL that they spit out.

Okay, so...

So that's how I would assume it would work.

Okay.

So...

For this one database, this needs to be existed, right?

Like I do not.

I'm not.

Yes, you can.

Okay.

Um, yeah, yeah.

Yeah.

Actually, I'm creating it, but it's not like it's...

Technically, something is being done.

It's created in service count, but you don't have to worry about that.

It's just, a database has to exist in order for you to turn DMS on.

So that's requirement one, because it has all the info in order to turn it on, right?

Like, it needs the closer you are or the closer endpoint, the closer soma, the database name, the all that other jazz.

Once the database exists and is functional, at that point, you now have the ability to turn on DMS for said database.

You take some of those values from the database, and you pipe it through the create app service again. To then create the DMS stuff, and then based off that, lifecycle of DMS, it'll either be provisioning or completed or failed.

So.

Perfect.

Yeah, those are, it's pretty simple, it seems, like, behind the sky.

Okay, see.

Um.

Okay, so far, I liked it.

So now let's say that DMS has been created, like this URL.

And database, uh, enabled it, like whoever this, this is enabled for this particular database.

Then my button goes gray, right?

Like you can't do...

I don't know.

Are there requirements on the, you can't turn it off?

Like, is it like a one way binding?

Like, you turn it on and that's it?

I believe that.

Yep.

Okay, so from a UI standpoint, you need to make sure that once it's enabled, they cannot, like, unenable it until we get that requirement.

So however you decide to do that on the UI, giving you all the freedom to make that decision.

Okay, so.

Uh, okay, so next question.

So let's say that it happened.

Like it is enabled now.

It could literally just be a button that says enable and you click it, and then when it's done, there's just no button on the screen again.

It just shows the information about Deimos.

Can I show that?

So that information I showed to the user.

And then now, let's say, the user comes to the database, to the workspace page.

Like whatever, in this case, whatever, need to test.

Let's say that.

Unless we get that, unless we get that requirement, then call out the requirement, then I wouldn't just start guessing.

Start guessing.

Okay.

It seems like, according to them, it's on the database, so when they go to the database, that's where they'll see the DMS stuff for set database.

So it's not like another...

Yes, it is another service catalog entry.

Uh, we might have to do something from our ingestion standpoint, which you might need to note this down, to skip ingesting that event and skip ingesting that, uh, type of resource.

Otherwise, it will end up in the catalog.

So they'll have, like, a DMS entry.

Yeah, I don't see any DMS entries.

Unless, uh, would you be able to call, um, on the business application?

Is this for Eddie?

Can you call, like, get all application services for this one?

And does it come up in that list?

It didn't for me yesterday, but yeah, but you can run that one to see.

Because yesterday we did create some, right?

Right now we have one in the database.

Yeah, so you're talking about this one, right?

Yeah, it doesn't show up in this list, right?

It does.

Oh, it does.

Okay.

So, yeah, so, Russia, you'll want to, as just a hidden requirement or...

I mean, if it shows up in the catalog, I don't know what.

Like, stipulations are with that, but I feel like it would be weird to show up in the catalogs, so you'll probably want to add to the ingestion.

Um, I'm also not sure you'll have to double check what, um, event, because they do event events when things are created.

I think right now we listen on Rosa.

Yeah, I see in one other thing.

Very cool thing.

For topic I had seen.

So you want to make sure that A, are we already listening to a database one?

If we are, then you'll need to add in additional logic to essentially skip ingesting, like, DNS is, like, a catalog entry, and you're just gonna use it as, like, kind of a metadata on an existing thing, like, an existing database.

Or like.

Until they tell us otherwise.

Okay.

It, um, should be good, so those get the two things I'd say.

It's just.. It really does call, get the status of DMS, nicely display, how to turn it on, if it's not turned on, when it's turned on, have the different states, like, is it in the process of being configured?

Has it been configured?

If so, is there now a URL I can go to?

Or something, some nice way of displaying that, and then not allowing them to turn it off?

And then the last thing would be, double check the ingestion points, both from a topic standpoint, and an application is, like, provider standpoint, and just make sure that we're not ingesting the DMS stuff. As a catalog entry.

Okay.

Should be good, and then all the info that you need to call this should already be on the database there.

Um, so, you just essentially take all that output that's required?

Those, like, four things, and then pipe it on through again to eat them, and then that's how you do what you need to do.

Okay, thank you.

I think I got it.

No, you did it.

Okay.

Uh, what is my question, then?

Yeah, okay.

So even though it in the, it looks like that catalog did, the catalog has this one, I don't have to show it in through the UI.

Even though it is there.

Right?

I mean, yeah, I would say it doesn't make sense.

I know why it's a whole separate resource, but I'm an idiot.

Okay, so right now, if I go to the UI, the test one, I will not see this.

I think I win.

Even though, because I have not done it.

Well, if this is if this is Eddie's branch, it's whatever branch, like if you're pointing to his branch, and it would be local host, you may or may not see it.

I don't know how you have your locals set up.

I don't know any of that.

But by default, I'm pretty confident it would show up unless you did logic to tell it not to.

Yeah, I didn't do anything, like, um...

So...

Okay, I'm going to go and check my service, not running right now.

Any other questions or do you need stuff written down?

I don't know if Kelly was taking notes of some of that.

No, but next time I will.

Good, Ab.

Yeah, well.

Well, if anything, like, you don't quite recall or if you need me to write something down, just let me know.

Okay.

Hopefully, hopefully, does that make sense to everybody, like, what I went over, hopefully, and, like, forget anything?

Yeah, it makes sense to me.

Yeah.

Okay.

Okay, um, yeah.

Okay, if I have any other thing, like if I forget, like I try to pin it down, but then I will contact you, Dylan.

So late, I do the whole thing.

AI also going so stupid.

I tell you, it just messes things up.

If I don't tell him, like, if I don't give the right prompt, Um, But yeah.

And the day I do something, like that has to give me something.

So, and you know, when I asked this AI yesterday, that it is like this Leo thingy, and it told me that 0 um, 0 event.

This is what told me.

So I'm like, what?

And then when you when you said that, I went to the U provider code and then I see that 4 topics are there.

So I told that to AI, and he says, either is right.

I'm like, what?

It was like 4.5, um, solid, I guess.

It was that model.

Oh, keys.

So I'll take it from here, denotate everything, and, um, Yeah, so that this button would be on the managed page.

This is what Dan came for like a minute and he wanted me to show my screen.

So he went through that UI and he wanted that button should be on the managed tab of database.

Okay.

Okay.

All right.

Well, just let me know if you need anything or anything. Questions or any thoughts on stuff, I guess?

Okay, thank you, guys.

Thank you all.

Thank you.

Thanks.

I'm gonna open up a merger request, which is gonna, like, temporarily break a branch, so...

Was this transcription useful or not useful?
