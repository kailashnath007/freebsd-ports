# Created by: Sunpoet Po-Chuan Hsieh <sunpoet@sunpoet.net>
# $FreeBSD$

PORTNAME=	Net-DNS-TestNS
PORTVERSION=	1.10
PORTREVISION=	2
CATEGORIES=	dns perl5
MASTER_SITES=	CPAN
MASTER_SITE_SUBDIR=	CPAN:OLAF
PKGNAMEPREFIX=	p5-

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Perl extension for simulating simple Nameservers

BUILD_DEPENDS=	p5-Net-DNS>=0.64:${PORTSDIR}/dns/p5-Net-DNS \
		p5-XML-LibXML>=1.53:${PORTSDIR}/textproc/p5-XML-LibXML
RUN_DEPENDS:=	${BUILD_DEPENDS}

USE_PERL5=	configure
USES=		perl5

.include <bsd.port.mk>
