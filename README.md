# Envoy and .NET Core proof of concept

## Introduction

This is an attempt to create an http AuthZ filter for Envoy (and later, gRPC).

## Usage

Run ``docker-compose up --build`` to build and start the services.

Envoy sits in front of everything on port ``8000`` so use http://localhost:8000, which will result in a forbidden message.

If you add ``i_am_super_secret=yes`` as a query string, auth will succeed and the request will be forwarded to the service.