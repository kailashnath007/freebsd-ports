# $FreeBSD$

PORTNAME=	Dancer
PORTVERSION=	1.3132
PORTREVISION=	1
CATEGORIES=	www perl5
MASTER_SITES=	CPAN
MASTER_SITE_SUBDIR=	CPAN:YANICK
PKGNAMEPREFIX=	p5-

MAINTAINER=	kuriyama@FreeBSD.org
COMMENT=	Perl extension for minimal-effort oriented web application framework

LICENSE=	ART10 GPLv1
LICENSE_COMB=	dual

RUN_DEPENDS=	\
	p5-HTTP-Body>0:${PORTSDIR}/www/p5-HTTP-Body \
	p5-HTTP-Date>0:${PORTSDIR}/www/p5-HTTP-Date \
	p5-HTTP-Message>0:${PORTSDIR}/www/p5-HTTP-Message \
	p5-HTTP-Server-Simple-PSGI>0:${PORTSDIR}/www/p5-HTTP-Server-Simple-PSGI \
	p5-Hash-Merge-Simple>0:${PORTSDIR}/devel/p5-Hash-Merge-Simple \
	p5-libwww>0:${PORTSDIR}/www/p5-libwww \
	p5-MIME-Types>0:${PORTSDIR}/mail/p5-MIME-Types \
	p5-Module-Runtime>0:${PORTSDIR}/devel/p5-Module-Runtime \
	p5-Try-Tiny>0:${PORTSDIR}/lang/p5-Try-Tiny \
	p5-URI>0:${PORTSDIR}/net/p5-URI
BUILD_DEPENDS:=	${RUN_DEPENDS}

OPTIONS_DEFINE=	YAML
OPTIONS_DEFAULT=	YAML

.include <bsd.port.options.mk>

.if ${PORT_OPTIONS:MYAML}
RUN_DEPENDS+=	p5-YAML>0:${PORTSDIR}/textproc/p5-YAML
.endif

USES=	perl5
USE_PERL5=	configure
NO_ARCH=	YES

.include <bsd.port.mk>
