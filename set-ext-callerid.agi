#!/usr/bin/perl

# Copyright 2012 Marcin Adamowicz <martin.adamowicz@gmail.com>

# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at

# http://www.apache.org/licenses/LICENSE-2.0

# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

##### Description #####
# Simple Asterisk AGI for setting up CallerID for external calls.
# Dialplan required.


use warnings;

use Asterisk::AGI;

my $AGI = new Asterisk::AGI;
my %input = $AGI->ReadParse();

my $callerid = $ARGV[0];

	# Range 1800 - 1999
	if ( $callerid =~ /^1[8|9]\d\d/) {
		$AGI->set_variable('CALLERID(num)',"52586$callerid");
	}
	# Range 2000 - 2299
	elsif ($callerid =~ /^2[0-2]\d\d/) {
		$AGI->set_variable('CALLERID(num)',"52589$callerid");
	}
	# Range 4650 - 4699
	elsif ($callerid =~ /^46[6-9]\d/) {
		$AGI->set_variable('CALLERID(num)',"52584$callerid");
	}
	# Range 9300 - 9599
	elsif ($callerid =~ /^9[3-5]\d\d/) {
		$AGI->set_variable('CALLERID(num)',"52525$callerid");
	}

